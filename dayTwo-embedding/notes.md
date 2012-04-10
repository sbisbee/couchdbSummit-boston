Embedding
---------

  - CouchDB's replicator makes it ideal for embedding it onto different
    platforms (ex., mobile), but it's developed as a server (ex., MySQL) which
    does not allow for this very easily.

  - See SLEEP spec and comments from yesterday.

  - The ideal would be to pull out the core storage engine and use it like
    bitcask, allowing for easy and direct integration into erlang apps via
    erlang calls.

  - One of the big wins for CouchDB to do this is that more erlang people will
    be using our code and therefore (hopefully) contribute more code to us.

  - Rebar is may or may not work for us.

    - We need to figure out what the list is of things that autotools gives us.

    - Autotools makes it very easy for cross platform compile.

  - We don't necessarily need to change our build system. We can make it so
    that you can import our code into something like rebar.

  - We also need a clear, well documented erlang interface.

**The Results**

  - We're not interested in making the current CouchDB implementation
    embeddable onto other platforms like mobile. The answer to the is, and has
    been historically, re-implementations of protocols (ex., PouchDB).

  - We're going to create a clear and documented erlang interface for erlang
    developers to interface directly with the persistence engine.
