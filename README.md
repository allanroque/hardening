Ansible hardening
=========

This roles configure the Basic Hardening.

Included Adjusts:
 - Upgrade all packages
 - Install necessary Software
 - Remove undesirable packages
 - Stop and disable unnecessary services
 - Install and Cockpit
 - Install and configure motd and issue
 - Add hardened SSH config

Requirements
------------

None

Role Variables
--------------

```
unnecessary_services:
  - postfix
  - telnet
```

```
unnecessary_software:
  - tcpdump
  - wpa_supplicant
```

```
necessary_software:
  - net-tools
  - bind-utils
  - wget
  - vim
  - tree
  - sysstat
  - git
  - traceroute
```

```
cockpit_software:
  - cockpit
  - cockpit-dashboard
  - cockpit-system
  - cockpit-storaged
  - cockpit-bridge
  - cockpit-podman
  - cockpit-machines
  - cockpit-do
```

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - role: allanroque.hardening
```

License
-------

BSD

Author Information
------------------

https://github.com/allanroque/