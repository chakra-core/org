# Regex System

## Introduction

The Regex implementation within ChakraCore has a few seperate components:

- The Regex constructor object, prototype and library methods - these are implemented as part of the Javascript Library (inside lib/Runtime/Library) and call into the other Regex components when they need to.
- The Regex Parser lib/Parser/RegexParser.cpp invoked by the main parser at parse time (for Regex literals) OR the Regex Constructor at runtime. Analyses the Regex creating an abstract syntax tree for it including sets of characters for each operation.
- The Regex Pattern class lib/Parser/RegexPattern.cpp instances of this class are created when parsing a RegEx, and stored in an internal slot of any Js Regex object - they are then used whenever that Reh
- The Regex Compiler lib/Parser/RegexCompileTime.cpp processes the parser output creating a RegexProgramme - a sequence of instructions with attached data (sets of characters) to be executed whenever the Regex is used, the created Programme is stored as a property of the Regex Pattern.
- The Regex Runtime lib/Parser/RegexRuntime.cpp interpretor loop used for executing Regex programmes
- The Regex Stats tool lib/Parser/RegexStats.cpp debugging/testing tool used for outputting details about what Regex features are being used - has to be enabled with a compile time flag.

## The Parser

The Regex parser is invoked by the main JS parser on RegEx literals but also can be invoked at runtime by the Regex Constructor.

It can be invoked with buildAST = true or false:

- When buildAST = false it will simply check the syntax of the Regex, raising an exception if a syntax error is found or completing normally with no output if the syntax is correct.

- When buildAST = true it will both check the syntax AND create an Abstract Syntax Tree (AST) representing the RegEx pattern it has parsed. This AST consists of both the detail of the operations to be performed AND sets (instances of the class defined in lib/Parser/CharSet.cpp & lib/Parser/CharSet.h) of the characters relevant to the operations, IMPORTANT NOTE: these sets are fundamentally collections of 16bit characters. Any kind of match operation is implemented using a set of characters - e.g. the `.` wildcard in a RegEx is converted into a match set operation where the set contains all possible char16s excluding the newline characters that it `.` does not match.

## The Compiler

The Regex Compiler analyses the AST converting it into a sequence of internal operations (the available operations are listed in lib/Parser/RegExOpCodes.h) these operations are internally defined actions/abstracted ways of implementing RegEx operations and do not directly correlate with the specification.

Operations include walking forward until a match for a set is found, looking forward without moving, looking backwards etc. Each operation is created as an instance of an Instruction class (there is one such class per possible operation) with the relevant set of characters set as a property of the Instance. Note, the implementations of these operations are defined as ::exec methods inside lib/Parser/RegexRuntime.cpp.

The sequence of these instruction objects are stored in an instance of a Programme class (defined in lib/Parser/RegexRuntime.h) this is then attached as a property to the Regex Pattern object.

## The Runtime

The Regex runtime is invoked whenever a Regex match is performed e.g. by Regex.prototype.test or Regex.prototype.match etc. It implements a loop containing a switch statement with a case for every op code from RegExOpCodes.h - note these are included by using some #defines then including that header - it also contains exec methods for each op code that are called to execute them.
