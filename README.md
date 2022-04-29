![Ansible Lint](https://github.com/johanneskastl/ansible-role-add_zypper_repository/workflows/Ansible%20Lint/badge.svg)

add_zypper_repository
=========

Add a zypper repository

Requirements
------------

None.

Role Variables
--------------

- `repository_name`: (required) the name of the new repository, also used as filename
- `repository_baseurl`: (required) the URL of the new repository
- `repository_enabled`: (optional) in case you want to add the repository, but disable it, set this to `0`
- `autorefresh_enabled`: (optional) in case you want to disable autorefresh of the repository, set this to `0`
- `priority`: (optional) per default, the priority is set to `99`
- `gpgcheck`: (optional) per default, gpg checks are enabled, but can be disabled by setting this to `0`
- `keeppackages`: (optional) in case you want to disable the `keeppackages` option, set this to `0`

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.add_zypper_repository'
          vars:
            repository_name: 'repo-oss'
            repository_baseurl: 'http://download.opensuse.org/tumbleweed/repo/oss/'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
