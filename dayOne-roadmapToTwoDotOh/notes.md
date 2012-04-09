Roadmap to CouchDB 2.0
----------------------

  - Smaller, more incremental releases. Will include breaking changes. No more
    "big honking releases".
  - Time based releases?
    - Only works if you have a lot of communication.
  - Odd/even version numbers?
    - Linux kernel dropped this.
    - Allows people to test things out.
    - Can be confusing.
  - People seem to generally like release candidates.
  - Disagreement over semver. Jan calls for order (loudest voice).
  - We need to be able to test the combination of feature branches.
  - Shorten the timing between releases.
  - Nightly releases please!
  - The goal is to introduce code freezes when only bug fixes can be landed.
  - Re-use nightly tarballs as the votable artifacts.

**Version Numbers and Breaking Changes**
  - We need to release breaking changes more quickly.
  - Use Node.JS as a model.
  - Version numbers aren't as important as releasing.
  - We will break things. It's called progress.
  - The upgrade path should be a defined file format that you can
    import/export.
  - We need to figure out LTS, how long, etc. The timelines need to overlap.

**2.0 and What Does the Major Number Mean**
  - Moving forward the industry is going to be using different databases for
    different problems. We don't need to be all things to all people.
  - We're going to have a log warning for deprecated features. "This feature
    you're using won't work in the next release."

**The Results**
  - Release branches are always stable (release-able).
  - Faster, time based releases.
  - Need to define what a LTS is.
  - Promote nightly releases.
  - Whenever a major or minor release is made, the previous version branch is
    going to be also released with deprecation warnings.
  - We need a prioritized list of features. Here is a list of features that we
    already know we want, not in a prioritized order:
    - BigCouch
    - Faster bulk insert tooling (direct to disk? binary?) as long as it
      doesn't invalidate the HTTP API.
    - npm for couchdb plugins
    - ...return to this tomorrow...
