Fail2ban
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.fail2ban-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/fail2ban)
[![Build Status](https://travis-ci.org/samdoran/ansible-role-fail2ban.svg?branch=master)](https://travis-ci.org/samdoran/ansible-role-fail2ban)

Install and configure [Fail2ban](http://www.fail2ban.org/wiki/index.php/Main_Page).

Currently only the `sshd` jail file is configured.

Requirements
------------

- EPEL repository enabled
- Firewall configured and running

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `fail2ban_jail_path` | `/etc/fail2ban/jail.d` | Directory where jail files are copied |
| `fail2ban_ignore_ips` | `127.0.0.1/8` | List of IPs to ignore. |


Dependencies
------------

- `samdoran.repo-epel`

Example Playbook
----------------

    - hosts: all
      roles:
        - samdoran.repo-epel
        - samdoran.firewall
        - samdoran.fail2ban

License
-------

MIT
