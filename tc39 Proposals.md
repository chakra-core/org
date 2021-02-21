# TC39 Stage 3 and 4 Proposals with ChakraCore Implementation status

TC39 proposals are proposals for new features or significant changes to Javascript. Stage 4 proposals are finalised and have either been published as part of the Javascript specification or are due for imminent publication as such. Stage 3 proposals are proposals that are ready for implementation with minor refinements to be made based on feedback from the implementation process but are otherwise considered complete.

Stage|CC Status|CC Ref|Proposal|Author|Champion(s)|Expected Publication Year|
| --- | --- | --- | --- | --- | --- | ---|
|4|In 1.11 |n/a| [`Array.prototype.includes`][array-includes]| Domenic Denicola| Domenic Denicola<br />Rick Waldron| 2016|
|4|In 1.11 |n/a| [Exponentiation operator][exponentiation]| Rick Waldron| Rick Waldron| 2016|
|4|In 1.11|[PR][Object-values-entries-pr]| [`Object.values`/`Object.entries`][object-values-entries]| Jordan Harband| Jordan Harband| 2017|
|4|In 1.11|[PR][String-padding-pr] | [String padding][string-padding] | Jordan Harband | Jordan Harband<br />Rick Waldron| 2017|
|4|In 1.11|[PR][Object-getOwnPropertyDescriptors-pr]| [`Object.getOwnPropertyDescriptors`][object-gopds] | Jordan Harband<br />Andrea Giammarchi| Jordan Harband<br />Andrea Giammarchi | 2017|
|4|In 1.11|n/a| [Trailing commas in function parameter lists and calls][function-commas] | Jeff Morrison| Jeff Morrison | 2017|
|4|In 1.11|n/a| [Async functions][async-await] | Brian Terlson| Brian Terlson | 2017|
|4|Disabled behind flag|[Implementation][Implement-Shared] [Flag][Disable-Shared] | [Shared memory and atomics][atomics] | Lars T Hansen| Lars T Hansen | 2017|
|4|Not Started|[Issue][Template-literal-issue] | [Lifting template literal restriction][template-literal-lift]| Tim Disney | Tim Disney| 2018|
|4|In master|[PR][RegExp-dotall-PR] | [`s` (`dotAll`) flag for regular expressions][dot-all] | Mathias Bynens | Brian Terlson<br />Mathias Bynens | 2018|
|4|Not Started|[Issue][Regexp-named-capture-issue] | [RegExp named capture groups][named-groups]| Gorkem Yakin<br />Daniel Ehrenberg | Daniel Ehrenberg<br />Brian Terlson<br />Mathias Bynens | 2018|
|4|In master|[PR][Object-rest-spread-PR] | [Rest/Spread Properties][object-rest-spread] | Sebastian Markbåge | Sebastian Markbåge| 2018|
|4|Not Started|[Issue][Regexp-lookbehind-assertions-issue] | [RegExp Lookbehind Assertions][lookbehind] | Gorkem Yakin<br />Nozomu Katō<br />Daniel Ehrenberg| Daniel Ehrenberg<br />Mathias Bynens| 2018|
|4|Not Started|[Issue][Regexp-unicode-escapes-issue] | [RegExp Unicode Property Escapes][unicode-escapes] | Mathias Bynens | Brian Terlson<br />Daniel Ehrenberg<br />Mathias Bynens | 2018|
|4|In 1.11|[PR][Promise-finally-PR] | [`Promise.prototype.finally`][finally] | Jordan Harband | Jordan Harband| 2018|
|4|In master|[PR][async-iteration-PR] | [Asynchronous Iteration][async-iteration]| Domenic Denicola | Domenic Denicola| 2018|
|4|In master|[PR][Optional-catch-PR] | [Optional `catch` binding][optional-catch] | Michael Ficarra| Michael Ficarra | 2019|
|4|In master|[PR][JSON-super-PR] | [JSON superset][json-superset] | Richard Gibson | Mark Miller<br />Mathias Bynens | 2019|
|4|In master|[PR][Symbol-description-PR] | [`Symbol.prototype.description`][symbol-description] | Michael Ficarra| Michael Ficarra | 2019|
|4|In master|[PR][Function-toString-PR] | [`Function.prototype.toString` revision][function-to-string] | Michael Ficarra| Michael Ficarra | 2019|
|4|In master|[PR][Object-fromEntries-PR] | [`Object.fromEntries`][object-from-entries]| Darien Maillet Valentine | Jordan Harband<br />Kevin Gibbons | 2019|
|4|In master|[PR][Wellformed-stringify-PR] | [Well-formed `JSON.stringify`][well-formed-stringify]| Richard Gibson | Mathias Bynens| 2019|
|4|In master|[PR][String-trim-PR] | [`String.prototype.{trimStart,trimEnd}`][trims]| Sebastian Markbåge | Sebastian Markbåge<br />Mathias Bynens| 2019|
|4|In master|[PR][Array-flat-PR] | [`Array.prototype.{flat,flatMap}`][flat] | Brian Terlson<br />Michael Ficarra<br />Mathias Bynens | Brian Terlson<br />Michael Ficarra| 2019|
|4|Not Started|[Issue][String-replaceAll-Issue] | [`String.prototype.matchAll`][matchall]| Jordan Harband | Jordan Harband| 2020|
|4|Flagged in 1.11 enabled in Master|[PR][Dynamic-import-PR] | [`import()`][dynamic-import] | Domenic Denicola | Domenic Denicola| 2020|
|4|WIP|[Issue][BigInt-Issue] | [`BigInt`][bigint] | Daniel Ehrenberg | Daniel Ehrenberg| 2020|
|4|In master|[PR][Promise-allSettled-PR] | [`Promise.allSettled`][allsettled] | Jason Williams<br />Robert Pamely<br />Mathias Bynens| Mathias Bynens| 2020|
|4|In master|[PR][globalThis-PR] | [`globalThis`][globalThis] | Jordan Harband | Jordan Harband| 2020|
|4|Not Started| | [`for-in` mechanics][for-in-mechanics] | Kevin Gibbons| Kevin Gibbons | 2020|
|4|WIP|[Issue][Optional-chaining-issue] | [Optional Chaining][chaining]| Gabriel Isenberg<br />Claude Pache<br />Dustin Savery| Gabriel Isenberg<br />Dustin Savery<br />Justin Ridgewell<br />Daniel Rosenwasser |2020|
|4|In Master|[PR][Nullish-coallescing-PR] | [Nullish coalescing Operator][nullish-coalescing]| Gabriel Isenberg | Gabriel Isenberg<br />Justin Ridgewell<br />Daniel Rosenwasser |2020 |
|4|In master|[PR][Import-meta-PR] | [`import.meta`][import-meta] | Domenic Denicola | Gus Caplan| 2020|
|4|Not Started|[Issue][String-replaceAll-Issue] | [`String.prototype.replaceAll`][replace-all] | Peter Marshall<br />Jakob Gruber<br />Mathias Bynens| Mathias Bynens| 2021 |
|4|WIP|[PR][Promise-any-PR] | [`Promise.any`][promise-any] | Mathias Bynens<br />Kevin Gibbons<br />Sergey Rubanov | Mathias Bynens| 2021 |
|4|Not Started| | [WeakRefs][weakrefs] | Dean Tribble<br />Sathya Gunasekaran| Dean Tribble<br />Mark Miller<br />Till Schneidereit<br />Sathya Gunasekaran<br />Daniel Ehrenberg | 2021 |
|4|Not Started| | [Logical Assignment Operators][logical-assignment] | Justin Ridgewell| Justin Ridgewell <br /> Hemanth HM| 2021|
|4|In master|[PR][numeric-seperator-PR] | [Numeric separators][numeric_separators] | Sam Goto<br />Rick Waldron| Sam Goto<br />Rick Waldron| 2021|
|3|Not Started| | [Legacy RegExp features in JavaScript][regexp-legacy]| Claude Pache| Mark Miller<br />Claude Pache |
|3|Not Started| | [Private instance methods and accessors][private-methods]| Daniel Ehrenberg| Daniel Ehrenberg<br />Kevin Gibbons |
|3|Not Started|[Issue][class-fields-issue] | [Class Public Instance Fields & Private Instance Fields][class-fields] | Daniel Ehrenberg<br />Kevin Gibbons | Daniel Ehrenberg<br />Jeff Morrison<br />Kevin Smith<br />Kevin Gibbons |
|3|Not Started| | [Static class fields and private static methods][static-class-features]| Daniel Ehrenberg<br />Kevin Gibbons<br />Jeff Morrison<br />Kevin Smith | Shu-Yu Guo<br />Daniel Ehrenberg|
|3|In master|[PR][hashbang-PR] | [Hashbang Grammar][hashbang-grammar] | Bradley Farias| Bradley Farias| 
|3|In master|[PR][top-level-await-pr] | [Top-level `await`][await] | Myles Borins| Myles Borins|
|3|Not Started| | [RegExp Match Indices][regex-match-indices]| Ron Buckton | Ron Buckton |
|3|Not Started| | [`Atomics.waitAsync`][nonblocking] | Lars Hansen | Shu-yu Guo<br />Lars Hansen |
|3|In Master|[PR][at-pr] |[`.at()`][at]|Shu-yu Guo<br />Tab Atkins| Shu-yu Guo<br />Tab Atkins|
|3|Not Started| | [Import Assertions][import-assertions] | Myles Borins<br />Sven Sauleau<br />Dan Clark<br />Daniel Ehrenberg | Myles Borins<br />Sven Sauleau<br />Dan Clark<br />Daniel Ehrenberg | 
|3|Not Started| | [JSON Modules][json-modules] | Myles Borins<br />Sven Sauleau<br />Dan Clark<br />Daniel Ehrenberg | Myles Borins<br />Sven Sauleau<br />Dan Clark<br />Daniel Ehrenberg |
|3|Not Started| | [Ergonomic brand checks for Private Fields][private-fields-in-in]| Jordan Harband| Jordan Harband|

[import-assertions]: https://github.com/tc39/proposal-import-assertions
[json-modules]: https://github.com/tc39/proposal-json-modules
[private-fields-in-in]: https://github.com/tc39/proposal-private-fields-in-in
[at]: https://github.com/tc39/proposal-relative-indexing-method
[array-includes]: https://github.com/tc39/Array.prototype.includes
[exponentiation]: https://github.com/tc39/proposal-exponentiation-operator
[object-values-entries]: https://github.com/tc39/proposal-object-values-entries
[string-padding]: https://github.com/tc39/proposal-string-pad-start-end
[object-gopds]: https://github.com/tc39/proposal-object-getownpropertydescriptors
[function-commas]: https://github.com/tc39/proposal-trailing-function-commas
[async-await]: https://github.com/tc39/ecmascript-asyncawait
[atomics]: https://github.com/tc39/ecmascript_sharedmem
[template-literal-lift]: https://github.com/tc39/proposal-template-literal-revision
[dot-all]: https://github.com/tc39/proposal-regexp-dotall-flag
[named-groups]: https://github.com/tc39/proposal-regexp-named-groups
[object-rest-spread]: https://github.com/tc39/proposal-object-rest-spread
[lookbehind]: https://github.com/tc39/proposal-regexp-lookbehind
[unicode-escapes]: https://github.com/tc39/proposal-regexp-unicode-property-escapes
[finally]: https://github.com/tc39/proposal-promise-finally
[async-iteration]: https://github.com/tc39/proposal-async-iteration
[optional-catch]: https://github.com/tc39/proposal-optional-catch-binding
[json-superset]: https://github.com/tc39/proposal-json-superset
[symbol-description]: https://github.com/tc39/proposal-Symbol-description
[function-to-string]: https://github.com/tc39/Function-prototype-toString-revision
[object-from-entries]: https://github.com/tc39/proposal-object-from-entries
[well-formed-stringify]: https://github.com/tc39/proposal-well-formed-stringify
[trims]: https://github.com/tc39/proposal-string-left-right-trim
[flat]: https://github.com/tc39/proposal-flatMap
[matchall]: https://github.com/tc39/String.prototype.matchAll
[dynamic-import]: https://github.com/tc39/proposal-dynamic-import
[allsettled]: https://github.com/tc39/proposal-promise-allSettled
[bigint]: https://github.com/tc39/proposal-bigint
[globalThis]: https://github.com/tc39/proposal-global
[for-in-mechanics]: https://github.com/tc39/proposal-for-in-order
[chaining]: https://github.com/tc39/proposal-optional-chaining
[nullish-coalescing]: https://github.com/tc39/proposal-nullish-coalescing
[import-meta]: https://github.com/tc39/proposal-import-meta
[regexp-legacy]: https://github.com/tc39/proposal-regexp-legacy-features
[tests-regexp-legacy]: https://github.com/tc39/test262/issues/2371
[class-fields]: https://github.com/tc39/proposal-class-fields
[tests-class-fields]: https://github.com/tc39/test262/issues/1161
[numeric_separators]: https://github.com/tc39/proposal-numeric-separator
[private-methods]: https://github.com/tc39/proposal-private-methods
[weakrefs]: https://github.com/tc39/proposal-weakrefs
[nonblocking]: https://github.com/tc39/proposal-atomics-wait-async
[replace-all]: https://github.com/tc39/proposal-string-replaceall
[static-class-features]: http://github.com/tc39/proposal-static-class-features/
[await]: https://github.com/tc39/proposal-top-level-await
[hashbang-grammar]: https://github.com/tc39/proposal-hashbang
[richer-keys]: https://github.com/tc39/proposal-richer-keys
[regex-match-indices]: https://github.com/tc39/proposal-regexp-match-Indices
[resource-management]: https://github.com/tc39/proposal-using-statement
[standard-library]: https://github.com/tc39/proposal-javascript-standard-library
[private-declarations]: https://github.com/tc39/proposal-private-declarations
[promise-any]: https://github.com/tc39/proposal-promise-any
[logical-assignment]: https://github.com/tc39/proposal-logical-assignment

[Object-values-entries-pr]: https://github.com/microsoft/ChakraCore/pull/171
[String-padding-pr]: https://github.com/microsoft/ChakraCore/pull/174
[Object-getOwnPropertyDescriptors-pr]: https://github.com/microsoft/ChakraCore/pull/1202
[Implement-Shared]: https://github.com/microsoft/ChakraCore/pull/2939
[Disable-Shared]: https://github.com/microsoft/ChakraCore/commit/ee2538d7b38be8093d9c9341d761d4e8267050bc
[Template-literal-issue]: https://github.com/microsoft/ChakraCore/issues/2344
[RegExp-dotall-PR]: https://github.com/microsoft/ChakraCore/pull/5592
[Regexp-named-capture-issue]: https://github.com/microsoft/ChakraCore/issues/3928
[Object-rest-spread-PR]: https://github.com/microsoft/ChakraCore/pull/6130
[Regexp-lookbehind-assertions-issue]: https://github.com/microsoft/ChakraCore/issues/3448
[Regexp-unicode-escapes-issue]: https://github.com/microsoft/ChakraCore/issues/2969
[Promise-finally-PR]: https://github.com/microsoft/ChakraCore/pull/4668
[async-iteration-PR]: https://github.com/microsoft/ChakraCore/pull/6312
[Optional-catch-PR]: https://github.com/microsoft/ChakraCore/pull/5310
[JSON-super-PR]: https://github.com/microsoft/ChakraCore/pull/6211
[Symbol-description-PR]: https://github.com/microsoft/ChakraCore/pull/5828
[Function-toString-PR]: https://github.com/microsoft/ChakraCore/pull/5446
[Object-fromEntries-PR]: https://github.com/microsoft/ChakraCore/pull/5622
[Wellformed-stringify-PR]: https://github.com/microsoft/ChakraCore/pull/6206
[String-trim-PR]: https://github.com/microsoft/ChakraCore/pull/5693
[Array-flat-PR]: https://github.com/microsoft/ChakraCore/pull/5573
[String-replaceAll-Issue]: https://github.com/microsoft/ChakraCore/issues/6297
[Dynamic-import-PR]: https://github.com/microsoft/ChakraCore/pull/6233
[BigInt-Issue]: https://github.com/microsoft/ChakraCore/issues/5440
[Promise-allSettled-PR]: https://github.com/microsoft/ChakraCore/pull/6138
[globalThis-PR]: https://github.com/microsoft/ChakraCore/pull/5885
[Optional-chaining-issue]: https://github.com/microsoft/ChakraCore/issues/6349
[Nullish-coallescing-PR]: https://github.com/chakra-core/ChakraCore/pull/6545
[Import-meta-PR]: https://github.com/microsoft/ChakraCore/pull/6156
[class-fields-issue]: https://github.com/microsoft/ChakraCore/issues/6136
[hashbang-PR]: https://github.com/microsoft/ChakraCore/pull/6145
[numeric-seperator-PR]: https://github.com/microsoft/ChakraCore/pull/6143
[top-level-await-pr]: https://github.com/chakra-core/ChakraCore/pull/6457
[Promise-any-PR]: https://github.com/microsoft/ChakraCore/pull/6301
[at-pr]: https://github.com/chakra-core/ChakraCore/pull/6610
