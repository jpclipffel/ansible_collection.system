# # Ansible Role - jpclipffel.system.sshd

Configures the SSH server.

The role runs only on supported OS. If run on an unsupported OS, the role
does nothing.

The following OS are supported:

| OS      | Distribution | Versions  | Notes |
|---------|--------------|-----------|-------|
| `linux` | `ubuntu`     | `>=18.04` |       |

## Tags

| Tag        | Description                            |
|------------|----------------------------------------|
| `setup`    | Installs and configures the SSH server |
| `teardown` | Stops the SSH server                   |
| `remove`   | Stops and remove the SSH server        |

## Variables
