# Ansible check_mk_agent role

This is an [Ansible](http://www.ansible.com) role to install check_mk agent.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Facts

Te role provides the following facts:

- `check_mk_agent_dir`: agent directory
- `check_mk_agent_plugins_dir`: plugins directory
- `check_mk_agent_host_added`: true when host was added
- `check_mk_agent_services_changed`: true when services changed
- `check_mk_agent_services_changes_applied`: true when changed were applied

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.check_mk_agent
```

## Testing

Tests are based on [molecule with podman containers](https://molecule.readthedocs.io/en/latest/installation.html).

Tests need role variable be defined. So, to run the tests you have to pass
extra variables/inventories:

```shell
cd amtega.check_mk_agent

molecule test -- --vault-id <id>@prompt -i <inventory_path>
```

## License

Copyright (C) 2023 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira
- Juan Antonio Valiño García
- Carlos Chedas Fernández
