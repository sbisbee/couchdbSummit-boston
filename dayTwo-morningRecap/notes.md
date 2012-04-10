Day Two, Morning Recap
----------------------

  - Some confusion about the couchapp resolution from yesterday.

    - We're going to remove the couchapp specific code from "core" (data store
      with replication and a view server on the side) and make it a plugin that
      is shipped with CouchDB by default.

    - Will not break current show/list functions, creating the possibility for
      further expansion in the future. A deeper point of view is that we are
      breaking the apps out of the view server, preventing view rebuilds and
      row rescans, while allowing functionality to be added that would not be
      safe in the view server.

    - We acknowledge that we don't know everything that an application server
      would need or want.

    - One possible future is that every request is handled by a chain of
      modules, such as a couchapp module.

  - We need better tooling around couchapps and pushing design doc code. Make
    it easier for people to get started. Should be shipped with Apache CouchDB,
    creating a blessed tool set.

    - Keep it simple.

    - Use it in the "getting started" documentation.

    - Make sure it's cross platform. Might use erlang for this since we're
      already shipping the runtime, or something else. Maybe Futon with file
      APIs?
