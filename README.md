# Ansible Collection for Gitea

This collection includes roles to deploy Gitea with Podman and systemd.

## Installation

The collection can be installed with `ansible-galaxy`:

```sh
ansible-galaxy collection install git+https://github.com/ahaydon/ansible-gitea-collection.git
```

## Usage

```yaml
- role: gitea_podman
  gitea_podman_user: gitea
  gitea_podman_home: /home/gitea
  gitea_podman_mariadb_root_passwd: "{{ gitea_password }}"
  gitea_podman_db_passwd: "{{ gitea_password }}"
```

## License

This Ansible collection is [MIT licensed](LICENSE).
