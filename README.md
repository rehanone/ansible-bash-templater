ansible-bash-templater
=========

An ansible role for managing the installation of `bash-templater`.

More information on `bash-templater` tool can be found at:

  - [https://github.com/vicentebolea/bash-templater](https://github.com/vicentebolea/bash-templater)


Requirements
------------

This role requires git to be installed on the target system.

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: rehanone.bash_templater
      vars:
        templater:
          debug: true
          state: present
          install_directory: '/opt/bash-templater'
          binary_directory: '/usr/local/bin'
          repo_source: 'https://github.com/vicentebolea/bash-templater.git'
          repo_revision: master
      when: templater_manage
```

License
-------

Apache-2.0
