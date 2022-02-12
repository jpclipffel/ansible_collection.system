# Ansible role: `system_dns`

Configure the local DNS resolution.

The role runs only on supported OS. If run on an unsupported OS, the role
does nothing.

The following OS are supported:

| OS      | Distribution | Versions | Notes |
|---------|--------------|----------|-------|
| `linux` | -            | -        |       |

## Tags

| Tag     | Description                |
|---------|----------------------------|
| `setup` | Setup local DNS resolution |

## Variables

See `defaults/main.yml` for the full list of variables.

| Variable                         | Type     | Required | Defaut        | Description                         |
|----------------------------------|----------|----------|---------------|-------------------------------------|
| `jpclipffel_system_dns_resolver` | `string` | No       | `resolv.conf` | `systemd-resolved` or `resolv.conf` |
| `jpclipffel_system_dns_servers`  | `list`   | No       | `[]`          | List of DNS servers                 |
| `jpclipffel_system_dns_options`  | `list`   | No       | `[]`          | List of DNS options                 |
| `jpclipffel_system_dns_domains`  | `list`   | No       | `[]`          | List of DNS domains                 |


## Templates

| Template                   | Description                      |
|----------------------------|----------------------------------|
| `resolv.conf.j2`           | `resolv.conf` template           |
| `systemd-resolved.conf.j2` | `systemd-resolved` configuration |
