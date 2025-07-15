<!--
SPDX-FileCopyrightText: 2022 Alexander Dahl <alex@netz39.de>
SPDX-License-Identifier: CC-BY-4.0
-->

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.3] - 2025-07-15

### Added

- Let Renovate (Bot) update pre-commit and github workflow dependencies
  ([#26](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/26),
  [#30](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/30))

### Changed

- Update pre-commit and github workflow dependencies
  ([#27](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/27),
  [#28](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/28),
  [#32](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/32),
  [#33](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/33),
  [#34](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/34),
  [#38](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/pull/38))

### Fixed

- Improve docker image availability check
  ([#17](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/issues/17))

## [0.2.2] - 2025-03-06

### Added

- Prevent role execution failure on architectures without Telegraf Docker image
  ([#17](https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/issues/17))

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

[unreleased]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.2.3...HEAD
[0.2.3]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.2.2...v0.2.3
[0.2.2]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.2.1...v0.2.2
[0.2.1]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/LeSpocky/ansible-role-telegraf-docker-in-docker/releases/tag/v0.1.0
