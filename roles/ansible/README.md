# Ansible role - jpclipffel.system.ansible

Configure the Ansible account.

Four _services_ are configured:

| Service    | Tasks file           | Description                                           |
|------------|----------------------|-------------------------------------------------------|
| `ssh`      | `tasks/ssh.yml`      | Ansible account's SSH keys                            |
| `sudo`     | `tasks/sudo.yml`     | Ansible account's `sudo` configuration                |
| `pip`      | `tasks/pip.yml`      | Setup Python's `pip` packages manager                 |
| `password` | `tasks/password.yml` | Enable or disable Ansible account login with password |

The role runs only on supported OS. If run on an unsupported OS, the role
does nothing.

The following OS are supported:

| OS      | Distribution | Versions  | Notes |
|---------|--------------|-----------|-------|
| `linux` | `ubuntu`     | `>=18.04` |       |

## Tags

| Tag        | Description           |
|------------|-----------------------|
| `setup`    | Install configuration |
| `teardown` | Remove confguration   |
| `remove`   | Remove confguration   |

## Variables

See `defaults/main.yml` for the full list of variables.

| Variable                                      | Type           | Required | Defaut               | Description                       |
|-----------------------------------------------|----------------|----------|----------------------|-----------------------------------|
| `jpclipffel_system_ansible_user_name`         | `string`       | No       | `{{ ansible_user }}` | Ansible account name              |
| `jpclipffel_system_ansible_public_keys_files` | `list[string]` | No       | _Empty list_         | Ansible account public keys files |
| `jpclipffel_system_ansible_public_keys`       | `list[string]` | No       | _Empty list_         | Ansible account public keys       |

## Templates

| Template             | Description                                          |
|----------------------|------------------------------------------------------|
| `sudoers-ansible.j2` | `sudoers` file template for the Ansible user account |
