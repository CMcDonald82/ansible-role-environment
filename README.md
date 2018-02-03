# ansible-role-environment

[![Build Status](https://travis-ci.org/CMcDonald82/ansible-role-environment.svg?branch=master)](https://travis-ci.org/CMcDonald82/ansible-role-environment)

Ansible role for configuring environment variables on an Ubuntu server

This role adds environment variables to /etc/environment

## Requirements

None

## Role Variables

```
environment_file: /etc/environment
```

The file where the environment variables will be located. On an Ubuntu system, this default location is probably best.

```
environment_vars: {}
```

The map of environment variables, in the format VARIABLE: value

## Example Playbook

```
- name: Set environment variables on Ubuntu server
  hosts: all
  remote_user: "{{ remote_username }}"
  become: yes

  roles:
    - role: environment_role
      environment_vars:
        TEST_VAR: test
        EXAMPLE_VAR: example
``` 

## Dependencies

None