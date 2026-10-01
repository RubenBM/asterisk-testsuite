================================================================================
                         Asterisk Test Suite
                         Personal Downstream Fork
================================================================================

This repository is a personal downstream fork of the official Asterisk Test
Suite, maintained by RubenBM as an independently controlled copy of the
upstream project.

The primary purpose of this fork is to retain an independently controlled copy
of the Asterisk Test Suite for personal development, testing, and contingency
purposes.

This repository is NOT an official Asterisk project repository and is not
affiliated with or endorsed by the Asterisk project or Sangoma Technologies
Corporation.


UPSTREAM
--------------------------------------------------------------------------------

Official Asterisk Test Suite:
    https://github.com/asterisk/testsuite

Asterisk:
    https://github.com/asterisk/asterisk

Asterisk Documentation:
    https://docs.asterisk.org/

Asterisk Project:
    https://www.asterisk.org/

The master branch is intended to remain reasonably synchronized with upstream
when practical. Upstream changes may be incorporated periodically rather than
continuously.


PURPOSE
--------------------------------------------------------------------------------

This fork provides:

  * An independently controlled copy of the Asterisk Test Suite
  * A downstream location for personal testing and development
  * A means of validating downstream Asterisk changes
  * A contingency copy should independent maintenance become necessary

At present, there is no requirement for this repository to maintain a separate
downstream test framework or permanent patch set.

Substantial or reusable modifications may instead be developed in separate
branches or repositories as appropriate.


RELATIONSHIP TO ASTERISK
--------------------------------------------------------------------------------

The Asterisk Test Suite provides external, automated functional testing for
Asterisk.

The Asterisk source repository is maintained separately:

    https://github.com/RubenBM/asterisk

Keeping the Asterisk source and test suite in separate repositories preserves
their upstream project boundaries while allowing each to be independently
synchronized and maintained.


USING THE TEST SUITE
--------------------------------------------------------------------------------

The test suite is intended to test an Asterisk installation or build.

Requirements and available tests vary with the version of the test suite,
Asterisk, operating system, and selected tests.

Before running the suite, review the repository configuration, dependency
requirements, and documentation applicable to the version being used.

The primary test runner is:

    ./runtests.py

To list available tests:

    ./runtests.py -l

To display command-line help:

    ./runtests.py --help

A specific test can be selected using the test runner's supported options.

The repository also provides the run-local helper for setting up and running
tests against a local Asterisk source tree:

    ./run-local setup
    ./run-local run

Refer to the scripts, configuration files, and test documentation in this
repository for current usage.


TEST DEVELOPMENT
--------------------------------------------------------------------------------

The test suite contains external functional tests for Asterisk.

Tests generally reside under:

    tests/

A test normally contains a run-test executable together with any configuration,
supporting files, or other resources required by the test.

Test configuration is defined using YAML files where applicable.

The repository contains examples and supporting configuration under:

    configs/
    sample-yaml/

When developing or modifying tests, follow the conventions established by the
existing test suite and verify the test against the applicable Asterisk
versions and configurations.


DOWNSTREAM DEVELOPMENT
--------------------------------------------------------------------------------

Future downstream work may include:

  * Test fixes
  * Additional tests
  * Environment-specific testing
  * Compatibility changes
  * Tests supporting downstream Asterisk modifications

There is intentionally no permanent downstream patch structure at this time.

If this fork develops substantial divergence from upstream, its repository
structure and documentation will be updated accordingly.


KEEPING THE FORK CURRENT
--------------------------------------------------------------------------------

The upstream Asterisk Test Suite repository is the authoritative source for
the project.

A typical synchronization workflow is:

    git remote add upstream https://github.com/asterisk/testsuite.git
    git fetch upstream
    git checkout master
    git merge upstream/master

The exact synchronization method may vary depending on downstream work.

Changes specific to this fork should generally be kept separate from the
upstream-tracking branch whenever practical.


DOCUMENTATION
--------------------------------------------------------------------------------

For authoritative information about the Asterisk Test Suite, refer to the
upstream repository and Asterisk documentation:

    https://github.com/asterisk/testsuite
    https://docs.asterisk.org/
    https://www.asterisk.org/


RELATIONSHIP TO HOME INFRASTRUCTURE
--------------------------------------------------------------------------------

This repository is maintained as a standalone software repository.

The test suite may be used as part of testing Asterisk within my broader home
production infrastructure, but deployment-specific infrastructure, networking,
monitoring, backups, and other operational configuration belong in the
corresponding infrastructure projects.

This separation keeps the test suite reusable and avoids coupling it to a
particular deployment.


LICENSING AND ATTRIBUTION
--------------------------------------------------------------------------------

This repository retains the upstream Asterisk Test Suite licensing, copyright,
authorship, and attribution information.

Refer to COPYING and the repository's other licensing and attribution files
for the applicable terms.

Asterisk and related marks are trademarks of Sangoma Technologies Corporation.

This personal fork is not affiliated with, endorsed by, or operated by
Sangoma Technologies Corporation or the official Asterisk project.


ACKNOWLEDGMENTS
--------------------------------------------------------------------------------

This repository is based on the Asterisk Test Suite project and incorporates
the work of its contributors.

Original authorship, copyright, licensing, and attribution remain applicable
to the upstream code contained in this repository.


--------------------------------------------------------------------------------
Personal downstream fork of the Asterisk Test Suite.

For authoritative project information and current technical documentation,
refer to the official Asterisk project.
--------------------------------------------------------------------------------
