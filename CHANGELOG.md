# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a
Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres
to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.2.10] - 2024-05-21

* hostFact() - now supports dotted facts, kinda-sorta

## [2.2.9] - 2024-04-22

* puppetdb-fact - bug fixes (had left a debugging 'exit 0')

## [2.2.8] - 2024-04-16

* puppetdb-fact - json output is now parseable by jq, which seems like a win
* puppetdb-hosts - looking for networking.fqdn rather than fqdn

## [2.2.7] - 2023-05-19

* puppetdb-fact - handles rarely-used structured facts better (have to
  parse the inventory endpoint data)

## [2.2.6] - 2023-03-22

* __init__.py - added references to the inventory endpoint for API v4
* puppetdb-fact - added support for dotted facts (e.g. os.release.major)
  using the inventory endpoint

## [2.2.5] - 2021-09-23

* puppetdb-stats - new script, look at metrics endpoint data from the
  puppetdb server, meant for use with check\_mk, still experimental

* puppetdb-fact-json - new script, queries puppetdb for a few specific
  facts and outputs them as human-readable json, for easy reading

## [2.2.4] - 2020-12-16

* __init__.py - 'AND' -> 'and' in nodesFailed() (this was causing problems
  with newer puppetdb)

## [2.2.3] - 2020-11-16

* lint fixes
* fixed a lot of bad calls to raise exceptions

## [2.2.2] - 2020-02-25

* added CentOS 8 support (mostly Requires and BuildRequires changes)
* __init__.py - setting to stronger SSL by default
* puppetdb-uuid-by-host - completely reworked to use the `partitions`
  fact, which is a default puppet fact so should be more useful to others

## [2.2.1] - 2019-08-19

### Changed

* ran all python through flake8 python linter, cleaned it up to match

### Changed

## [2.2.0] - 2019-08-16

* puppetdb-report-usage - added disk data
* converted all scripts and libraries to Python 3.

## [2.1.4] - 2019-03-19

### Added

* CHANGELOG.md - standardizing on a single changelog file

### Changed

* Makefile.local - now includes Pypi (pip) bindings
* setup.py, omdclient.spec - re-worked for setuptools instead of distutils.core
* README.md - lots of updates on the path towards real distribution
* `usr/sbin/*` moved to `usr/bin/*` (it just plays nicer with python)

