<!--
SPDX-FileCopyrightText: 2022 Alexander Dahl <alex@netz39.de>
SPDX-License-Identifier: CC-BY-4.0
-->

# Telegraf Docker in Docker

[![REUSE status](https://api.reuse.software/badge/git.fsfe.org/reuse/api)](https://api.reuse.software/info/git.fsfe.org/reuse/api)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

Ansible Role for running Telegraf Agent with Docker input plugin in Docker container.

## Requirements

Uses a task of type [community.docker.docker_container
module](https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html).

## Role Variables

### Mandatory Variables

* `tdid_influxdb_org`:
  * Description: InfluxDB organization name.
* `tdid_influx_token`:
  * Description: InfluxDB API token.
    Recommended to not put this into the playbook, but use vault or
    secure lookup!

### Optional Variables

* `tdid_data_dir`:
  * Default: `"/srv/data/telegraf"`
  * Description: The destination directory on the host, where the role
    copies the configuration file to.
* `tdid_docker_image`:
  * Default: `"telegraf:latest"`
  * Description: Combination of "telegraf" and some tag.
    Default uses the latest image from
    [Docker Hub](https://hub.docker.com/_/telegraf/).
  * Examples:
    * `"telegraf:latest"`
    * `"telegraf:alpine"`
    * `"telegraf:1.23"`
    * `"telegraf:1.24-alpine"`
* `tdid_influxdb_url`:
  * Default: `"http://localhost:8086"`
  * Description: URL of the node running InfluxDB node.
* `tdid_influxdb_bucket`:
  * Default: `"default"`
  * Description: Destination bucket to write into.
* `tdid_timezone`:
  * Default: `"UTC"`
  * Description: Environment variable `TZ` passed to the telegraf container.
  * Examples:
    * `Europe/Berlin`
    * `Asia/Nepal`

## Dependencies

No other galaxy roles used, just the community module listed above.

## Example Playbook

Just include the role and set some [variables](#role-variables).

### Minimal Example

```yaml
- hosts: servers
  roles:
    - role: telegraf_docker_in_docker
      vars:
        tdid_influxdb_org: Home
        tdid_influx_token: "{{ lookup( … ) }}"
```

### Full Example

```yaml
- hosts: servers
  roles:
    - role: telegraf_docker_in_docker
      vars:
        tdid_influxdb_org: Home
        tdid_influx_token: "{{ lookup( … ) }}"
        tdid_data_dir: /srv/data/telegraf
        tdid_influxdb_bucket: devops
        tdid_influxdb_url: "http://influx.example.org:8086"
        tdid_docker_image: telegraf:1.24-alpine
        tdid_timezone: "Europe/Berlin"
```

## License

This project is licensed unter the [MIT License](LICENSES/MIT.txt) unless noted differently in the file and adheres to [REUSE compliance](https://api.reuse.software/info/git.fsfe.org/reuse/api).

© 2022 [Alexander Dahl](https://github.com/LeSpocky) and contributors


## Author Information

Written by [Alexander Dahl](mailto:alex@netz39.de) for
[Netz39](https://www.netz39.de/) infrastructure monitoring.
