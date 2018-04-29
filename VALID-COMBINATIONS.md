# Introduction
There are quiet a few variables and combinations possible. This is an attempt
to explain what combinations are valid. You can also review the options in
vars/main.yml, and all tests are described in molecule/defaults/playbook.yml.

# OpenJDK

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution|release         |java_version   |
|------------|----------------|---------------|
| alpine     | 3.6 & 3.7      | 7 & 8         |
| archlinux  | base           | 7, 8, 9 & 10  |
| CentOS     | 6 & 7          | 6, 7 & 8      |
| Debian     | 8 (jessie)     | 7             |
| Debian     | 9 (stretch)    | 8             |
| Debian     | 10 (buster)    | 8 & 9         |
| Fedora     | 26 & 27        | 8 & 9         |
| OpenSUSE   | 42.2 & 42.3    | 7 & 8         |
| Ubuntu     | 17.10 (artful) | 8 & 9         |
| Ubuntu     | 18.04 (bionic) | 8, 9, 10 & 11 |

# Oracle

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution     |release     |java_version|java_type  |java_format|
|-----------------|------------|------------|-----------|-----------|
| Any             | Any        | 8, 9 & 10  | jre & jdk | targz     |
| CentOS & Fedora | Any        | 8, 9 & 10  | jre & jdk | rpm       |
