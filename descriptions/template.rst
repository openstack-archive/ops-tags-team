# This is a template that can be used for creating new tags. At a minimum
# the following information should be submitted when creating a tag.
#
# Each tag should have a the following structure:
# - descriptions/<tag_name>.rst - Description of the tag
# - <release_name>/<tag_name>.json - Tag definition
#
# All comment lines (marked with a '#') should be removed before submission.

========================================================================
ops:<tag_name>
========================================================================

# Introductory paragraph
# Provide a short summary of what this tag will mean


Rationale
=========

# Provide a detailed explanation of why the OpenStack ecosystem benefits
# from having this tag defined.

Requirements
============

# Provide a list of requirements for granting the tag to an existing
# project.
# All the criteria should be objective and predictable.
# If a tag requires another tag, this should be mentioned here.
#
# - Requirement 1
# - Requirement 2

Tag application process
=======================

# Details of the process to follow to maintain the tag. Are additions/
# removals regularly reviewed, or are they considered only upon request?
# Which group is involved, and at which frequency ?
#
# The process may include requiring feedback from specific groups,
# delegation of tag maintenance from the UC, minimum delays between
# application and tag grant, timeframes where granting or removing the
# tag is appropriate, etc.
#
# If the grant process is different from the removal process, this should
# also be mentioned here.
#
# By default, you can use the following process:
#
# Anyone may propose adding or removing this tag to a set of projects by
# proposing a change to the openstack/ops-tags-team repository. The change is
# reviewed by the Ops Tags Group and approved using standard resolution
# approval rules.
#
# - Step 1
# - Step 2
# - Step 3

Tag updates and timing
======================

# Ops Tags are typically made on a per-release basis.  Near the end
# of a release cycle, a new directory to contain the JSON files for
# the release is created, and tags are re-assessed.  Information is
# either removed or copied from the previous release as appropriate.
#
# Some tags may have a deprecation period (where a project retains the
# tag but only until a certain announced date). If the proposed tag has
# a deprecation period, its duration (and any other specific rules) should
# be listed here.
#
# - There is no deprecation period required for this tag.
# - It can be added or removed at any time.

Attributes
==========

# Tags may have attributes which provide extra information. Those attributes
# (and their values) should be described in this section
#
# - attribute1  - attribute1 description
# - attribute2  - attribute2 description
# - attribute3  - attribute3 description
