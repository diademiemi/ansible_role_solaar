Ansible Role Solaar
=========

[![Molecule Test](https://github.com/diademiemi/ansible_role_solaar/actions/workflows/molecule.yml/badge.svg)](https://github.com/diademiemi/ansible_role_solaar/actions/workflows/molecule.yml)

This is an Ansible role to install solaar, the Linux Logitech Unifying Receiver utility.

This role imports my `diademiemi.epel` role for RHEL systems.  

On Ubuntu, RHEL systems and Fedora the latest version of solaar is installed from Solaar supported repositories. On Debian, the Solaar version may be outdated.  

Requirements
------------
These platforms are supported:
- Ubuntu 20.04  
- Ubuntu 22.04  
- Debian 10  
- Debian 11  
- EL 8 (Tested on Rocky Linux 8)  
- EL 9 (Tested on Rocky Linux 9)  
- Fedora 38  

<!-- 
- List hardware requirements here  
-->

Role Variables
--------------

Variable | Default | Description
--- | --- | ---
<!--
`variable` | `default` | Variable example
`long_variable` | See [defaults/main.yml](./defaults/main.yml) | Variable referring to defaults
`distro_specific_variable` | See [vars/debian.yml](./vars/debian.yml) | Variable referring to distro-specific variables
-->

Dependencies
------------
<!-- List dependencies on other roles or criteria -->
None

Example Playbook
----------------

```yaml
- name: Use solaar role
  hosts: "{{ target | default('solaar') }}"
  roles:
    - diademiemi.solaar
```

License
-------

MIT

Author Information
------------------

- diademiemi (@diademiemi)

Role Testing
------------

This repository comes with Molecule tests for Docker on the supported platforms.
Install Molecule by running
```bash
pip3 install -r requirements.txt
```

Run the tests with
```bash
molecule test
```

These tests are automatically ran by GitHub Actions on push. If the tests are successful, the role is automatically published to Ansible Galaxy.

