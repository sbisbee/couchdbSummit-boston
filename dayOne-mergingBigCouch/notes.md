BigCouch Merge Plan
-------------------

  - Why does Cloudant want to do this?

    - It'll make Cloudant's life easier.

    - Be good citizens.

    - It's also beneficial for CouchDB so that it can scale in different ways.
      Example, no more "ouchDB".

    - BigCouch is really an extension that also has a bunch of optimizations
      and fixes, which CouchDB in its current form would benefit from. 

  - All of the things that we'd need to do to merge BigCouch in are things we
    should do in CouchDB anyways.

  - Full commits are weird in CouchDB and get weirder with distributed nodes.

  - Upgrade path:

    - Previously always relied on replication to go between CouchDB and
      BigCouch.

    - When you add the second node, bootstrap into clustered mode.

    - ...?

  - Adam/Paul explain how BigCouch works in erlang world.

  - "There's not much code to this." --Paul Davis

**The Results**

  - One repo and release, not two.

  - People need to think about what they're touching when developing CouchDB
    in the short term. And please talk to Paul Davis and Co. if you're making
    big changes.

  - Futon will need to be figured out (per node, cluster level, etc.).

  - The plan is to shape the BigCouch merge so that it can ship with CouchDB
    code and not break anything.
