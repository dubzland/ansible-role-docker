# Ansible Role: Docker
[![Gitlab pipeline status (self-hosted)](https://git.dubzland.net/dubzland/ansible-role-docker/badges/master/pipeline.svg)](https://git.dubzland.net/dubzland/ansible-role-docker)

Installs and configures Docker.

## Requirements
Ansible version 2.0 or higher.

## Role Variables

Available variables are listed below, along with their default values (see
    `defaults/main.yml` for more info):

### dubzland_docker_obsolete_packages
```yaml
dubzland_docker_obsolete_packages:
  - docker
  - docker-engine
  - docker.io
```

List of packages that previously installed Docker Engine.

### dubzland_docker_version

```yaml
dubzland_docker_version: ""
```

This needs to match the versioning of the package manager.  For Debian, this
will be something like `5:19.03.3~3-0~debian-stretch`.

### dubzland_docker_users

```yaml
dubzland_docker_users: []
```

List of users to be added to the `docker` group.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: docker
  become: yes
  roles:
  - role: dubzland-docker
```

## License

MIT

## Author

* [Josh Williams](https://codingprime.com)
