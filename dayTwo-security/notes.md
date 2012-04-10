Security
--------

  - Punt to third parties anything that isn't isAdmin?

  - Core is responsible for authorization, plugins can be responsible for
    authentication.

  - We're not a web framework.

  - Provide a clear mapping to plug the other authentication services into
    couch.

  - Basic and Cookie authentication are the only things we want to support in
    core/distrib.

  - Add the concept of where you're coming in from (localhost vs lan vs wan)
    and use it for authentication: even if you have the right creds, you won't
    be able to do admin things by default.

  - Have a fine grained matrix of privs per user. Ex., can compact, call
    /_restart, etc.

  - Move the _users database behind an API.

  - Side note, want per db configs (might consume _security)

  - We need to add on accounting/auditing (ex., sudo log).

  - Do we want to go with a global authentication system? NOT REINVENTING, but
    use something that's pre-existing.

**The Results**

  - We need to start from highly locked down and then increase the surface
    area over time or via config. (Analogies about trains, mathematics, etc.)

  - We will consider distributed identity, but it could also be added via
    plugins.
