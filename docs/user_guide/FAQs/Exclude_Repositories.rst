.. _Exclude_Repos:

Excluding Repositories
======================

By default, SIMP applies updates from all available repositories on a
nightly basis. This ensures that bug fixes and security updates are
applied to all systems without minute management in Puppet manifests.
This section provides guidance on how to include or exclude specific
repositories from nightly YUM updates.

Methodology
-----------

The *common::yum\_schedule::repos* and *common::yum\_schedule::disable*
variables in the pupmod-common module control which repositories are
enabled for nightly updating. Both variables must be specified in array
format.

*common::yum\_schedule::repos* is used to specify an array of
repositories from which updates are provided; no other repositories will
be used.

*common::yum\_schedule::disable* is used to specify an array of
repositories from which updates are not provided; all other repositories
will be used.
