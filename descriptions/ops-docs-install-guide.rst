========================================================================
ops:docs:install-guide
========================================================================

Is there a guide (at docs.openstack.org) that has installation
instructions for the project?

Rationale
=========

The existence of documentation that facilitates a basic installation of
a project is an important factor considered when adopting a project.

By making a general assessment for the software project's state of install
documentation based on distributions supported by the documentation team,
this tag provides the potential for at-a-glance information, especially
when used in conjunction with other tags, to determine a project's maturity.


Requirements
============


- Available - Guide exists, for all doc-team supported distributions for the
  release, can be used to perform a basic installation and does not suffer
  from major bugs.
- Not Available - No documentation exists for all supported distributions, or
  it suffers from major bugs that prevent it from being used to perform a
  basic installation.


Tag application process
=======================


- applied per major release by the ops tags team by checking
  docs.openstack.org, or through collaboration with the documentation team
- the docs team has a set of supported releases that should all have the same
  level. If there is a distro that is not at the same level (eg has a major
  bug), this should be noted in a caveat.
- where the status is not 'good', links to bugs must be provided.
- documentation typically lags the release, and major bugs are sometimes
  present for some time afterward. Reasonable efforts should be made to
  take this into account, with the focus always on providing the most
  information to the operator
- the application of this tag follows the distro classifications used by the
  documentation team (SUSE, RHEL/CentOS, Ubuntu) for their
  supported releases: the aim is a general guide to the existence of
  documentation - not an exhaustive distro-by-distro breakdown. Where there
  are differences between distributions or versions significant enough they
  would normally warrant a change in tag level, this should be noted in a caveat.

Tag updates and timing
======================

Ops Tags are typically made on a per-release basis. At around the end of a
release cycle, a new directory to contain the JSON files for the release is
created, and tags are re-assessed, copying or not using information from
the previous release as appropriate.

In the case of this tag, though it can be updated at any time, there are
four potential update times that would be more common, mostly surrounding
the release process and how documentation has traditionally been produced
and tested slightly lagging the release.

<-- potential for tag update here

1) OpenStack is released

<-- potential for tag update here

2) Docs are released

<-- potential for tag update here

3) Mass bug reports come in and docs are fixed.

<-- potential for tag update here

This will quite likely result in some period of time post-release where
documentation that will later be available is not. This is deemed useful
information to operators.


Attributes
==========

- status    - the tag application status
- bug_link  - URL(s) to major bugs afflicting a project's install
- description - optional details regarding the tag application
- caveats   - Any exceptions to the general status. Follows the same
              attributes as the general status, in addition to a 'label'
              attribute, which can be used as a title during display
