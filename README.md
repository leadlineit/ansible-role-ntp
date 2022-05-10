# Ansible Galaxy role for install and configure NTP server

![Build Status](https://github.com/leadlineit/ansible-role-ntp/actions/workflows/ansible-galaxy-ci.yml/badge.svg)
[![Galaxy Role](https://img.shields.io/badge/Ansible--Galaxy-leadlineit.ntp-blue.svg?logo=ansible&logoColor=white)](https://galaxy.ansible.com/leadlineit/ntp/)

This role helps to install and configure NTP server on a Debian (buster/bullseye).

Requirements
------------

This role requires Ansible 2.0 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
---
ntp_server:
  - ntp.exact-time.org
  - time.cloudflare.com
  - ntp1.itcompliance.dk
  - ntp.ea1145.net
```

You can pass 'ntp_restrict' and 'ntp_interface' variables (that are optional). It'll be skip, if not defined.

```yaml
---
ntp_restrict:
  - some.host.ip
ntp_interface:
  - some.host.ip
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: leadlineit.ntp, tags: ntp }
```

License
-------

MIT

Author Information
------------------

This role was created by Stas Stavnichuk.
