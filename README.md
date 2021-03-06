Ansible role: docker-ce
=========

Install docker-ce on Ubuntu 16.04, Debian 8.0, or Raspbian 8.0.
This role includes following tasks.

- Install docker and its requirements through apt (tags: always)
- Install recommended packages (tags: recommended)
- Start docker and enable/disable it (tags: always)
- Create docker group (tags: optional)

All the tasks need root privilege.

Requirements
------------

None.

Role Variables
--------------

Whether to start docker on boot (yes/no).

``` yaml
docker_service_enabled: yes
```

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
- hosts: all
  vars_files:
      - vars/main.yml
  roles:
      - {role: docker, become: yes}
```

License
-------

MIT

