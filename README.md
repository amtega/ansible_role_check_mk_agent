# Ansible check_mk_agent role

This is an [Ansible](http://www.ansible.com) role to install check_mk agent.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Facts

Te role provides the following facts:

- `check_mk_agent_changes_applied`: true if changes were applied, false if changes are pending of manual authorization

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.check_mk_agent
```

## Testing

Tests are based on docker containers. You can setup docker engine quickly using the playbook `files/setup.yml` available in the role [amtega.docker_engine](https://galaxy.ansible.com/amtega/docker_engine).

To run autojoin features test you need provide the variables defined in `defaults/main.yml` and the variable `check_mk_agent_autojoin_host` poininting to the host you want to use for testing. One way to provide this information is calling the testing playbook passing an additional plus the default one provided for testing, as it's show in this example:

```shell
$ cd amtega.check_mk_agent/tests
$ ansible-playbook main.yml -i inventory -i ~/mycustominventory.yml --vault-id myvault@prompt -e check_mk_agent_autojoin_host=host.acme.com
```

## License

Copyright (C) 2020 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira
