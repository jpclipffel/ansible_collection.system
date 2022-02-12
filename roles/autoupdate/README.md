# Ansible role - `system_autoupdate`

Configure the autoupdate mechanisms.

The role runs only on supported OS. If run on an unsupported OS, the role
does nothing.

The following OS are supported:

| OS      | Distribution | Versions  | Notes |
|---------|--------------|-----------|-------|
| `linux` | `ubuntu`     | `>=18.04` |       |

## Tags

| Tag        | Description                      |
|------------|----------------------------------|
| `setup`    | Setup autoupdate                 |
| `teardown` | Deactivate autoupdate            |
| `remove`   | Deactivate and remove autoupdate |

## Templates

| Template                 | Description                                  |
|--------------------------|----------------------------------------------|
| `unattended-upgrades.j2` | APT's unattended upgrades configuration file |
| `auto-upgrades.j2`       | APT's auto upgrades configuration file       |
