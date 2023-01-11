<!--
SPDX-FileCopyrightText: 2022 Alexander Dahl <alex@netz39.de>
SPDX-License-Identifier: CC-BY-4.0
-->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.1] - 2023-01-11

### Fixed

- Align documentation to code
- Make sure the configuration directory exists
  ([#15](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/issues/15))

## [0.2.0] - 2022-12-10

### Added

- Add quite some documentation
- Make system user name configurable (was fixed to 'telegraf' before)
  ([#6](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/issues/6))

### Changed

- Renamed variable `tdid_data_dir` to `tdid_conf_dir` and changed
  default value to */etc*
  ([#7](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/issues/7))

## [0.1.0] - 2022-11-29

### Added

- Add first running version

[0.2.1]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/releases/tag/v0.1.0
