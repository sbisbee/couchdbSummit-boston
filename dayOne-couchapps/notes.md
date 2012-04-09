Making a Better Couchapp Engine
-------------------------------

  - A few big issues with couchapps today:
    - Can't talk to the outside world.
    - Prototype tool or production system?
    - Auth/Auth

  - Allow the HTTP layer in CouchDB to be pluggable, allowing you to drop in a
    different framework. Instead of developing our own, half broken web
    framework.

  - Allow apps to replicate between databases and be aware of context (ex.,
    database of locations and a database of reviews).

  - Remove list and show functions from the core database API. Turn it into a
    plugin for couchapps. This would include removing them from the view
    server where they don't fit naturally (ex., don't have the same "no
    external sources" map function restrictions, can interact with the rest of
    the server, etc.).

  - Provide a standardized interface for things like couchapp plugins to be
    built on top of.

  - "How can we put couch on a weight loss program?" --Max Ogden

  - If we make things too modular then we're going to get into an issue of
    dependency management.

  - How do we build against what app devs want? Time saving?

  - API features will be different between platforms, but they'll all speak
    replication and store/understand data the same way.

  - couchapps were originally designed to be sandboxed.

  - We're a database that stores and serves application code very well,
    compared to other databases that just store the application code.

  - Sync (replicator) is the most powerful and important aspect.

**The Results**

  - Remove the couchapp specific stuff. Make hooks for this and other stuff
    into CouchDB.

  - Draw the line at serving JSON and attachments from CouchDB.

  - How important are couchapps versus the rest of CouchDB?
