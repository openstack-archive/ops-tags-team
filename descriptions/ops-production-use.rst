========================================================================
ops:production-use
========================================================================

Provides general information to operators regarding the number of
deployments who are using a particular project in production.

Rationale
=========

This data allows operators to understand the level to which which projects
are generally/popularly adopted, and therefore which projects are likely
to have desirable or undesirable maturity characteristics for common cases.

Though this information is available in the user survey, placing a snapshot
of this information into the tag system allows it to be more easily
combined with other tags. The user survey data should still be published
and made widely available as normal.


Requirements
============

Status is a percentage, derived from the user survey's "What projects does
this deployment use?" question (format: ###%)


Tag application process
=======================

- start by aquiring the percentages of production deployments for each
  project from the "What project does this deployment use?" question of the
  latest user survey
- The user survey is currently released within a month or so of the software
  release. Given this is the best current state of understanding at around
  this post-release time, survey data should be paired with the tags for
  the new release.
- applied per major release by the ops tags team
- in the case of 'new' projects not covered by the survey, the value should
  remain blank rather than '0' until that information can be extrapolated
  from the user survey

Tag updates and timing
======================

Ops Tags are typically made on a per-release basis. At around the end of a
release cycle, a new directory to contain the JSON files for the release is
created, and tags are re-assessed, copying or not using information from
the previous release as appropriate.

In the case of this tag, though it could be updated at any time, the user
survey comes out normally one month after release. As such, the following
two update times are probable:

<-- potential for tag update here, using previous survey data, so it's ready
 for release with the best information we have

1) OpenStack is released

2) User Survey results released

<-- potential for tag update here, to update to the latest survey data

This will result in some period of time post-release where the user survey
data is 6 months old. However, given the choice between providing this aged
data and providing none at all, it is kinder to provide some data.

Attributes
==========

- status    - the percentage of production deployments
- caveats   - Any exceptions to the general status. Follows the same
              attributes as the general status, in addition to an optional
              'label' attribute, which can be used as a title during display
