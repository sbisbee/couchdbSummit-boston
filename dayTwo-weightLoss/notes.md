Weight Loss: What to Remove
---------------------------

  - One of the replicator end points.

    - Keep the new API (_replicator) and have it support one off replications
      (ie., self terminating db).

    - Or keep _replicate, providing something like ?ephemeral, and nuke
      _replicator. Has the benefit that we're not changing the default behavior
      of databases (self deleting docs).

  - all_or_nothing

  - _restart

  - _sleep

  - How long to keep old revs? missing revs

  - total_rows and offset fields in view results

  - temporary views

  - rotate view in and out (ie., production views can't be hit if they don't
    have an index on disk), requiring dev/pre-production views to be warmed by
    the server

[incomplete, need to look at Joan's notes for the rest]

**The Results**

  - Delete:

    - all_or_nothing

    - Use the old API, _replicate, instead of the new API, _replicator.

    - _restart

    - _sleep

    - temporary views (do them in browser)

    - list/show

    - default.ini/local.ini => defaults are internal and the ini file is just
      all commented out.

  - Address design docs [incomplete, need to look at Joan's notes for the rest]

[incomplete, need to look at Joan's notes for the rest]
