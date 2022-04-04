# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.9.0] - 2022-04-04
### Added
- Automatic calculation of the latest version available in the check_mk artifact directory. Related to https://gitlab-sistemas.xunta.local/ansible/roles/amtega.check_mk_agent/-/issues/4

### Changed
- Moved tests engine to podman

## [1.8.2] - 2022-03-11
### Changed
- Fixed error autojoining existing host.

## [1.8.1] - 2022-02-18
### Changed
- Fix install when artifact is defined but not downloaded

## [1.8.0] - 2022-02-17
### Changed
- Adapted for CentOS derived distros. Related to ansible/main#263

## [1.7.1] - 2022-02-04
### Changed
- Removed pipeline on shell tasks.

## [1.7.0] - 2022-02-02
### Changed
- Refactored download stuff
- Supported distros. Related to ansible/main#178

## [1.6.0] - 2021-11-08
### Added
- Added `check_mk_agent_dir` and `check_mk_agent_plugins_dir` facts.
