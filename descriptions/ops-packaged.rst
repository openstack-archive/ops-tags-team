========================================================================
ops:packaged
========================================================================

Provides information to operators regarding the existence and quality of
packages for the project in distributions like Red Hat/Fedora, Ubuntu
and openSUSE/SLES.


Rationale
=========

The vast majority of ops use packages for deployment, so the existence of high
quality, bug free packages is an important factor considered when adopting a
project.

By making a general assessment for the software project's state of packaging
based on distributions officially supporting OpenStack, this tag provides
information that was previously difficult to determine, substantially improving
the decision making process.


Requirements
============

- good = Packages without major bugs exist for at least three distribution families
- beginning = Packages without major bugs exist for at least one distribution family
- warning = Packages exist, but have major bugs for more than one distribution family
- no = no packages exist in official distribution repositories for this project



Tag application process
=======================

- applied per major release by the ops tags team
- information is gathered from operator experiences using the packages, in
  addition to anything discovered by the documentation team when writing the
  new release's install guide
- in the case of 'new' projects, a simple check for the package in each
  distribution's package management should suffice to select the level between
  'no' and 'beginning'
- where the status is not 'good', links to bugs must be provided.
- the default assumption is that packages are bug-free unless a major bug link
  can be provided.
- the application of this tag follows the three-package-management-system
  classification used by the documentation team (apt, yum, zypper): the
  aim is a general guide to the existence of packages - not an exhaustive
  distro-by-distro breakdown. Where there are differences between
  distributions or versions significant enough they would normally warrant
  a change in tag level, this should be noted in a caveat.

Tag updates and timing
======================
Ops Tags are typically made on a per-release basis. At around the end of a
release cycle, a new directory to contain the JSON files for the release is
created, and tags are re-assessed, copying or not using information from
the previous release as appropriate.

In the case of this tag, though it can be updated at any time, there are
four potential update times that would be more common, mostly surrounding
the release process and how packages have traditionally been produced
and tested slightly lagging the release.

<-- potential for tag update here, based on RC efforts by packagers

1) OpenStack is released

<-- potential for tag update here, based on what's there on release day

2) Packages are formally announced

<-- potential for tag update here, based on the package cut

3) Mass bug reports come in and packages are fixed.

<-- potential for tag update here

This will quite likely result in some period of time post-release where
packages that will later be available are not yet ready, or bug-ridden.
This is deemed useful information to operators.

Attributes
==========

- status    - the tag application status
- bug_link  - URL(s) to major bugs afflicting a project's packages
- description - optional details regarding the tag application
- caveats   - Any exceptions to the general 'status'. Follows the same
              attributes as the general status: 'status', 'bug_link',
              'description'. In addition a 'label' attribute could be defined
              to be used as a title during display.
