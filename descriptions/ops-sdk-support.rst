========================================================================
ops:sdk-support
========================================================================

Provides general information to users regarding the number of
software development kits (SDKs) which support a particular service project.

Rationale
=========

This data allows users to understand the level to which which projects
are generally/popularly supported in SDKs, and therefore which projects are
likely to be able to be relied on for application development.

This information is available from the individual SDK information pages,
though it is often difficult to extract, and nowhere is it provided in
aggregate level. Placing a snapshot of this information into the tag system
allows it to be more easily combined with other tags to provide high-level
overviews of maturity for projects.


Requirements
============

Status is an integer - the number of SDKs updated within the release cycle
that support the service project - derived from a survey of all SDKs,
listed at https://wiki.openstack.org/wiki/SDKs .



Tag application process
=======================

- For each SDK listed at https://wiki.openstack.org/wiki/SDKs, determine
  whether the SDK has been updated within the release cycle. Only SDKs
  updated within the release cycle are counted toward this tag.
- For the recently updated SDKs, determine the status of their support for
  each service project.
- For each service, count the number of those SDKs that support it and
  enter that number in as the 'status'.
- in the case of 'new' projects, the value should start at '0' until SDK
  support has been seen

Tag updates and timing
======================

Ops Tags are typically made on a per-release basis. At around the end of a
release cycle, a new directory to contain the JSON files for the release is
created, and tags are re-assessed, copying or not using information from
the previous release as appropriate.

In the case of this tag, though it could be updated at any time, adding
support for a new project in an SDK is a significant endeavour. As such
it is reasonable to update the tag only in conjunction with the release,
with exceptional updates on request.

Attributes
==========

- status    - the number of recently updated SDKs supporting the project
- caveats   - Any exceptions to the general status. Follows the same
              attributes as the general status, in addition to an optional
              'label' attribute, which can be used as a title during display
