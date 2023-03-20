[![Molecule Test](https://github.com/bwInfoSec/ansible-role-guacamole/actions/workflows/molecule-test.yml/badge.svg)](https://github.com/bwInfoSec/ansible-role-guacamole/actions/workflows/molecule-test.yml)

# bwinfosec.guacamole

This role installs and configures [Apache Gucamole](https://guacamole.apache.org/) on Debian based hosts.

# Platforms

- Ubuntu 20.04
- Debian 11

## Install

``` sh
ansible-galaxy install bwinfosec.guacamole
```

# Example Playbook
```yml
- name: Setup guacamole proxy
  hosts: guacamole
  become: true
  
  vars:
    guacamole_nginx_server_name: guacamole.example.com
    guacamole_docker_extension: true

  roles:
    - bwinfosec.guacamole
```

## Role Variables

All role variables can be found in [defaults/main.yml](defaults/main.yml).

## Notes

### LDAP

For LDAP set up, please check [this](https://kifarunix.com/setup-apache-guacamole-openldap-authentication/).


## Requirements

For any required dependencies are listed in [requirements.yml](requirements.yml).

To install them run

``` sh
ansible-galaxy install -vr requirements.yml
```

## Local Development

This role includes a *molecule* test to execute on Debian 11 and Ubuntu 20.04.

## Licensing

This work is licensed under the [EUPL 1.2](https://joinup.ec.europa.eu/collection/eupl/eupl-text-eupl-12).

