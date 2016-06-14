awscli
======

This role installs and configures awscli using pip package and, optionally, enables tab auto completion for awscli commands and sets up awscli's config file.

Role Variables
--------------

- `awscli_version`: The awscli version to install (default: 'latest')
- `awscli_enable_tab_completion`: If true, enables tab auto completion for awscli commands (default: True)
- `awscli_user`: User to configure awscli for (Ex: 'ubuntu')
- `awscli_group`: Group to configure awscli for (default: awscli_user)
- `awscli_access_key`: ACCESS_KEY_ID for awscli commands (default: '')
- `awscli_secret_key`: SECRET_ACCESS_KEY for awscli commands (default: '')
- `awscli_region`: Default AWS region for awscli commands (default: '')

Example Playbook
----------------

    - hosts: servers
      roles:
        - { 
          role: 'awscli',
          awscli_user: 'ubuntu',
          awscli_region: 'eu-west-1'
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/dpujadas/ansible-role-awscli.svg?branch=master)](https://travis-ci.org/dpujadas/ansible-role-awscli)