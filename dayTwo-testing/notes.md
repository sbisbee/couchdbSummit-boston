Testing
-------

  - Need to figure out what our current coverage is.

  - No browser specific question.

  - Moving all browser tests to CLI.

  - Need to figure out regression testing and interoperability. Ie., can 1.2.0
    replicate to and from 1.1.0? Do views have performance regression?

  - Can we land on just one language for writing tests?

    - JS for integration tests and erlang for unit tests?

  - jquery.couch.js isn't tested. Whether it's broken out of Apache CouchDB or
    a team is created for it, it needs tests to be included.

  - Absolutely need to test futon.js

  - Need to track coverage and test results for all the different tests.

  - Would be nice if test output, such as from Make, got pushed to a central
    repository for tooling.

  - Do we care that etap isn't maintained? Switch to eunit?

  - How are we going to test different nodes' communication (post bigcouch
    merge)?

  - What versions of erlang are we going to support? Can we drop R13?

  - We need a version matrix of interoperability.

  - Do we use Travis or ASF hosted Jenkins?

    - Travis only has one platform.

    - We are already on Travis.

    - ASF infra is going to take time.

    - Can we leverage all of the "private" Jekins installs? (cloudant,
      couchbase, etc.)

**The Results**

  - Interop matrix

  - Get a simple way to generate test coverage reports

  - Have a way to automate pushing test results to ASF CouchDB
