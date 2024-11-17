# Raspberry Pi OS Ansible Scripts

The following Ansible playbooks are available:

- [Local Web Server](web-server.yml)

## Update Raspberry Pi and Install pip | pipx | Ansible

```
sudo apt-get update \
&& sudo NEEDRESTART_MODE=a apt-get dist-upgrade --yes \
&& sudo apt-get -y install python3-pip \
&& sudo apt -y install pipx \
&& pipx ensurepath \
&& source ~/.bashrc \
&& pipx install --include-deps ansible \
&& sudo apt autoremove -y
```

## Copying Ansible Playbook to Raspberry Pi

This will copy the playbook to the Raspberry Pi's `~` directory.

Replace the following:

- `path/to/directory` is the path to the directory on your local machine.
- `username` is your username on the Raspberry Pi.
- `ip-address` is the IP address of the Raspberry Pi.

```
scp -r path/to/directory username@ip-address:~
```

## Running Ansible Playbook

```
ansible-playbook raspberrypi/{ansible-script}.yml
```
