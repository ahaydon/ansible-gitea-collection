Ansible Role: Gitea
=========

An Ansible role for deploying Gitea as a Podman container managed by systemd.

Requirements
------------

None.

Role Variables
--------------

```yaml
gitea_podman_name: gitea
gitea_podman_user: gitea
gitea_podman_group: "{{ gitea_podman_user }}"
gitea_podman_version: latest-rootless
gitea_podman_db_version: latest
gitea_podman_home: /home/gitea
```

Dependencies
------------

- [ahaydon.podman](https://github.com/ahaydon/ansible-podman-collection) is used by the `gitea_podman` role.

Example Playbook
----------------

```yaml
- name: Deploy Gitea
  hosts: all
  roles:
     - role: gitea_podman
       gitea_podman_home: /home/gitea
       gitea_podman_mariadb_root_passwd: "{{ gitea_password }}"
       gitea_podman_db_passwd: "{{ gitea_password }}"
```

License
-------

MIT

Author Information
------------------

This role was created by [Adam Haydon](https://github.com/ahaydon)
