<a href="https://skrepr.com/">
  <p align="center">
    <img width="200" height="100" src="https://skrepr.com/wp-content/uploads/2021/10/skrepr_logo_liggend.svg" alt="skrepr" />
  </p>
</a>
<h1 align="center">Ansible Role Promtail</h1>
<div align="center">
  <a href="https://github.com/skrepr/ansible-role-hostname/releases"><img src="https://img.shields.io/github/release/skrepr/ansible-role-hostname.svg" alt="Releases"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/blob/main/LICENSE"><img src="https://img.shields.io/github/license/skrepr/ansible-role-hostname" alt="LICENSE"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/actions/workflows/ci.yml"><img src="https://github.com/skrepr/ansible-role-hostname/actions/workflows/ci.yml/badge.svg" alt="CI"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/issues"><img src="https://img.shields.io/github/issues/skrepr/ansible-role-hostname.svg" alt="Issues"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/pulls"><img src="https://img.shields.io/github/issues-pr/skrepr/ansible-role-hostname.svg" alt="PR"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/commits"><img src="https://img.shields.io/github/commit-activity/m/skrepr/ansible-role-hostname" alt="Commits"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/stars"><img src="https://img.shields.io/github/stars/skrepr/ansible-role-hostname.svg" alt="Stars"/></a><a> </a>
  <a href="https://github.com/skrepr/ansible-role-hostname/releases"><img src="https://img.shields.io/github/forks/skrepr/ansible-role-hostname.svg" alt="Forks"/></a><a> </a>
</div>

# About

This Ansible role is used for getting logs from your host to Loki with Promtail.

It also has the ability to add custom Nginx config to extract detailed logs from Nginx with Promtail.

[![Ansible Role](https://img.shields.io/ansible/role/56457)](https://galaxy.ansible.com/skrepr/hostname)
[![Ansible Role](https://img.shields.io/ansible/role/d/56457)](https://galaxy.ansible.com/skrepr/hostname)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/56457)](https://galaxy.ansible.com/skrepr/hostname)

## Requirements

- SSH access to the server
- Docker installed
## Role Variables

```

loki_user: this is your basic_auth user
loki_password: this is where the bearer token should be placed
loki_url: this the url where loki is used. /api/prom/push is already added in the template!

```

## Dependencies

You will need to have Docker installed on the host. You can do that for example with [this](https://github.com/geerlingguy/ansible-role-docker) awesome role from Geerlingguy!

## Example Playbook

```yaml
#!/usr/bin/env ansible-playbook


- hosts: production
  become: true

  roles:
   - geerlingguy.docker
   - skrepr.promtail
```

## License

MIT / BSD

## Author Information

This role was created in 2022 by [Jeroen van der Meulen](https://github.com/jeroenvandermeulen), commisioned by [Skrepr](https://skrepr.com)
