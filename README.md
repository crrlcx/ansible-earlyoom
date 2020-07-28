# Ansible EarlyOOM

Install earlyoom from apt repository.

## Role Variables

`dpkg_force_overwrite_configs` — overwrite config files with new from package.

`earlyoom_enabled` — enable earlyoom service.
`earlyoom_package` — earlyoom package name.
`earlyoom_version` — earlyoom version number or 'latest'

Variables for template generation

```yml
earlyoom_config:
  min_memory: "5%"
  min_swap: "10%"
  report_time: 60
  avoid_regex: "(^|/)(init|systemd|supervisord|sshd)$"
```

## Example Playbook

```yml
- hosts: localhost
  remote_user: root
  become: yes
  roles:
    - ansible-earlyoom
```

## License

MIT License

## Author Information

Carrol Cox <carrol@protonmail.com>
