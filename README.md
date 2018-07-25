Ansible Role: Swiss Java Knife (SJK) ([lrk.ansible-role-sjk](https://galaxy.ansible.com/lrk/ansible-role-sjk/))
=========
[![Build Status](https://travis-ci.org/lrk/ansible-role-sjk.svg?branch=master)](https://travis-ci.org/lrk/ansible-role-sjk)

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
    # LATEST or specific version number.
    # Default value: LATEST
    # See https://mvnrepository.com/artifact/org.gridkit.jvmtool/sjk for available versions
    sjk_version: LATEST

    # true: use the full sjk binary (with mxdump)
    # false: use lighter sjk binary (without mxdump)
    # Default value: false
    sjk_use_sjkplus: false

    # SJK Binary destination path
    sjk_dest: '/opt/sjk/sjk-{{ sjk_version | lower }}'

    # Configure SJK binary owner
    # Default value: empty
    sjk_owner:

    # Configure SJK binary owner group
    # Default value: empty
    sjk_group:

    # Configure CHMOD for SJK binary
    # Default value: u=r,g=r,o=r
    sjk_chmod: "u=r,g=r,o=r"

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
