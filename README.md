<!--
SPDX-FileCopyrightText: 2022 Alexander Dahl
SPDX-License-Identifier: CC-BY-4.0
-->

Telegraf Docker in Docker
=========================

[![REUSE status](https://api.reuse.software/badge/git.fsfe.org/reuse/api)](https://api.reuse.software/info/git.fsfe.org/reuse/api)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

Ansible Role for running Telegraf Agent with Docker input plugin in Docker container.

Requirements
------------

Uses a task of type [community.docker.docker_container
module](https://docs.ansible.com/ansible/latest/collections/community/docker/docker_container_module.html).

Role Variables
--------------

*tbd*

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

*tbd*

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

*tbd*

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: servers
  roles:
    - role: telegraf_docker_in_docker
      vars:
        tdid_data_dir: /srv/data/telegraf
        tdid_influxdb_org: Home
        tdid_influx_token: "{{ lookup( … ) }}"
        # optional
        tdid_influxdb_bucket: devops
        tdid_influxdb_url: "http://influx.example.org:8086"
        tdid_docker_image: telegraf:1.24-alpine
        tdid_timezone: "Europe/Berlin"
```

License
-------

MIT

Author Information
------------------

Written by [Alexander Dahl](mailto:alex@netz39.de) for
[Netz39](https://www.netz39.de/) infrastructure monitoring.
