# Phansible Role: MongoDB

[![CI](https://github.com/phansible/role-mongodb/actions/workflows/ci.yml/badge.svg)](https://github.com/phansible/role-mongodb/actions/workflows/ci.yml)

An Ansible Role that installs [MongoDB](https://www.mongodb.com/) 9.0 Community Edition from MongoDB's official apt repository on Ubuntu and Debian, created with [Phansible](http://phansible.com/) in mind.

## Requirements

- Ubuntu 22.04, 24.04, 26.04 or Debian 12, 13 (x86_64, CPU with AVX)
- Ansible >= 2.15
- Root access or `become` on the target
- HTTPS access to repo.mongodb.org and pgp.mongodb.com

## Role Variables

None. The role writes `/etc/mongod.conf` with the data in `/var/lib/mongodb`, logs in `/var/log/mongodb/mongod.log`, and `mongod` listening on `127.0.0.1:27017`. The `mongod` service is started and enabled.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - role-mongodb
```

## License

This role is released under the terms of the license specified in the repository or if not specified, under the [MIT license](https://raw.githubusercontent.com/phansible/role-mongodb/master/LICENSE).

## Author Information

This role was created in 2015 by [The Phansible Team & Contributors](https://github.com/phansible/role-mongodb/graphs/contributors), credits go also to [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/) and source of inspiration.
