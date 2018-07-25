Ansible Role: Swiss Java Knife (SJK) ([lrk.sjk](https://galaxy.ansible.com/lrk/sjk/))
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
  ---
  # defaults file for ansible-role-sjk/

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
