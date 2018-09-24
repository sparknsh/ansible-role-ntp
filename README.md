# Ansible Role: NTP

#### Version: 1.0.0

[![pipeline status](https://gitlab.com/sparknsh/ansible-role-ntp/badges/master/pipeline.svg)](https://gitlab.com/sparknsh/ansible-role-ntp/commits/master)

Development of this project is managed in a private repository then pushed out to [GitLab](https://gitlab.com/sparknsh/ansible-role-ntp) and [GitHub](https://github.com/sparknsh/ansible-role-ntp) when we have a new version for you. If you have any issues please contact [sparknsh](https://www.sparknsh.com/contact?type=issue&name=ansible-role-ntp)

## Role Variables

```yaml
ntp_enabled: True
ntp_timezone:

ntp_servers: []

ntp_restrict: []
```

#### Example

```yaml
ntp_enabled: True
ntp_timezone: Etc/UTC

ntp_servers:
  - "time.nist.gov iburst"
  - "ntp1.npl.co.uk iburst"
  - "ntp.sydney.nmi.gov.au iburst"
  - "time.google.com iburst"

ntp_restrict:
  - "127.0.0.1"
  - "::1"
```

## Example Playbook

```yaml
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
     - { role: sparknsh.ntp }
```

## License

MIT

## Author Information

This role was created in 2018 by [sparknsh](https://www.sparknsh.com) at [Rebel Media, Inc.](https://www.rebelmedia.io/)
