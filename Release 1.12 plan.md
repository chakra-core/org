# Plan for Version 1.12

## Timing

The last feature release of ChakraCore occurred on 29th June 2018 (version 1.10) since then there have been numerous security update releases and 1 non-security bug fix release (1.11). There has however been significant feature work performed since that date all of which is unreleased.

We intend to release 1.12 as soon as practicable - ideally before summer 2021.

## Actions prior to release

We will endeavour to perform the below important work prior to issuing this first community release. If time permits additional work may be done.

1. Review major changes between 1.11 and master to generate an accurate set of release notes.

1. Review current master against JavaScript standards to identify major gaps including assessing against the tc39 list of stage 3 and stage 4 proposals and also testing with test262. Document the result of this review.

1. Review the API and update documentation.

1. Fix any key regressions from 1.11, notably https://github.com/chakra-core/ChakraCore/issues/6511

1. Run a fuzzer on the current code base and fix any serious bugs detected.

1. Determine release method - where will releases be posted? Who will post them? How will it be clear that this release is NOT supported by microsoft?
