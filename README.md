java
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-java.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-java)

Provides Java (either OpenJDK (default) or Oracle.) for your system.

Requirements
------------

- For openjdk: Access to a repository containing packages, likely on the internet.
- For oracle: Download the rpm's from the Oracle website and place then in the "files" directory. These files are not included because a license has to be accepted. Oracle website: http://www.oracle.com/technetwork/java/javase/downloads/index.html

Role Variables
--------------

- java_version: 6, 7, 8 or 9.
- java_type: openjdk or oracle.
- java_jdk: yes, true, no or false.

Valid combinations:
- java_version: 6, java_type: openjdk
- java_version: 7, java_type: openjdk
- java_version: 8, java_type: openjdk
- java_version: 8, java_type: oracle
- java_version: 9, java_type: oracle

Dependencies
------------

- robertdebock.bootstrap

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Example Playbook
----------------

```
- hosts: servers

  roles:
    - robertdebock.java
```

Install this role using `galaxy install robertdebock.java`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
