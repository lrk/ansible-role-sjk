Ansible Role: Swiss Java Knife (SJK) ([lrk.ansible-role-sjk](https://galaxy.ansible.com/lrk/ansible-role-sjk/))
=========
[![Build Status](https://travis-ci.org/lrk/ansible-role-sjk.svg?branch=master)](https://travis-ci.org/lrk/ansible-role-sjk)
[![Galaxy](https://img.shields.io/badge/galaxy-lrk.ansible--role--sjk-blue.svg)](https://galaxy.ansible.com/lrk/ansible-role-sjk)
![Ansible](https://img.shields.io/ansible/role/d/27795.svg)
![Ansible](https://img.shields.io/badge/dynamic/json.svg?label=min_ansible_version&url=https%3A%2F%2Fgalaxy.ansible.com%2Fapi%2Fv1%2Froles%2F27795%2F&query=$.min_ansible_version)

An Ansible Role that install [Swiss Java Knife (SJK)](https://github.com/aragozin/jvm-tools).

Supported OSes
--------------
- Centos 7

Requirements
------------

[Swiss Java Knife (SJK)](https://github.com/aragozin/jvm-tools) are:
- Java Development Kit (JDK) installed on your machine.

Role Variables
--------------

Available variables along with default values are listed below (see `defaults/main.yml`)

```yml
  ---
    # SJK binary version.
    # latest or specific version number.
    # Default value: latest
    # See https://mvnrepository.com/artifact/org.gridkit.jvmtool/sjk for available versions
    sjk_version: latest

    # true: use the full sjk binary (with mxdump)
    # false: use lighter sjk binary (without mxdump)
    # Default value: false
    sjk_use_sjkplus: false

    # SJK Binary destination path
    sjk_dest: '/opt/sjk/sjk{% if sjk_use_sjkplus is defined and sjk_use_sjkplus== true %}-plus{% endif %}-{{ sjk_version | lower }}'

    # Configure SJK binary owner
    # Default value: empty
    sjk_owner:

    # Configure SJK binary owner group
    # Default value: empty
    sjk_group:

    # Configure CHMOD for SJK binary
    # Default value: u=r,g=r,o=r
    sjk_chmod: "u=r,g=r,o=r"
   
    # The repository from which sjk is downloaded (optional)
    # Default: https://repo1.maven.org/maven2
    sjk_repo_url: null

    # The repository username for authentication
    # Default: None
    sjk_repo_username: null

    # The repository password for authentication
    # Default: None
    sjk_repo_password: null

```

Dependencies
------------

This role don't have dependencies.

Example Playbook
----------------

```
  - hosts: servers
    vars:
    roles:
      - lrk.sjk
```

License
-------

Apache License Version 2.0

References
----------
- [Swiss Java Knife (SJK)](https://github.com/aragozin/jvm-tools)

Author Information
------------------

This role was created by [Lrk](https://github.com/lrk).
