# Introduction
There are quiet a few variables and combinations possible. This is an attempt
to explain what combinations are valid. You can also review the options in
vars/main.yml, and all tests are described in molecule/defaults/playbook.yml.

# OpenJDK

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution|release                  |java_version  |
|------------|-------------------------|--------------|
| alpine     | latest & edge           | 7 & 8        |
| archlinux  | base                    | 7, 8, 9 & 10 |
| CentOS     | 6 & latest              | 6, 7 & 8     |
| Debian     | stable & latest         | 8            |
| Fedora     | latest                  | 8 & 9        |
| Fedora     | rawhide                 | 8            |
| Gentoo     | latest                  | 8            |
| OpenSUSE   | leap                    | 7 & 8        |
| OpenSUSE   | tumbleweed              | 8, 10 & 11   |
| Ubuntu     | 17.10 (artful) & latest | 8 & 9        |

# Oracle

distribution = ansible_distribution
release = ansible_distribution_major_version

|distribution     |release     |java_version|java_type  |java_format|
|-----------------|------------|------------|-----------|-----------|
| Any             | Any        | 8 & 10     | jre & jdk | targz     |
| CentOS & Fedora | Any        | 8 & 10     | jre & jdk | rpm       |
