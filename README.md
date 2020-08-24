ansible-role-vagrant-plugins
=========

Ansible role for installing vagrant plugins

Requirements
------------

- [Vagrant](http://www.vagrantup.com)
- [Ansible](http://www.ansible.com)

Role Variables
--------------

- `vagrant_plugins_plugins`
  - list plugins to install the latest.
- `vagrant_plugins_plugins_with_version`
  - list plugins to install with targeted version.

Dependencies
------------

None

Example Playbook
----------------

```yaml
    - hosts: localhost
      connection: local
      vars: 
        vagrant_plugins_plugins:
          - { name: vagrant-omnibus }
          - { name: sahara }
        vagrant_plugins_plugins_with_version:
          - { name: vagrant-digitalocean, version: 0.6.0 }
      roles:
        - kun432.vagrant-plugins
```

License
-------

MIT

Author Information
------------------

- Kuniaki Shimizu <k.shimizu@8d1w.com>
  - github: @kun432
  - twitter: @kun432
  - Qiita: @kun432
  - Hatena ID: kun432
- Jean-Pierre Matsumoto <jp@matsusoft.com>
