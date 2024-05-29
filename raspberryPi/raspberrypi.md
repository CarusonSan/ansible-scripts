# Raspberry Pi OS Ansible Scripts

The following Ansible playbooks are available:

- [Local Web Server](web-server.yml)

## Prerequisites

1. Install pipx:

```
sudo apt install pipx
```

2. Intall ansible-core:

```
1. pipx install --include-deps ansible-core
2. pipx ensurepath
```

## Copying Ansible Playbook to Raspberry Pi

This will copy the playbook to the Raspberry Pi's `~` directory.

Replace the following:

- `path/to/script` is the path to the script on your local machine.
- `username` is your username on the Raspberry Pi.
- `ip-address` is the IP address of the Raspberry Pi.

```
scp path/to/script username@ip-address:~
```

## Running Ansible Playbook

```
ansible-playbook raspberrypi/raspberrypi.yml
```
