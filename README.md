# ansible-scripts

## macOS Dev Environment

### Prerequisites

1. Install Developer Tools (Python 3.9):

- `xcode-select --install`

2. Create .zsh profile and add Python to PATH

- `echo 'export PATH="$HOME/Library/Python/3.9/bin:$PATH"' >> ~/.zshrc`

3. Configure Python/pip & install Ansible:

- `python3 -m pip install --upgrade pip`
- `python3 -m pip install --user ansible`

4. Adding JAVA_HOME to .zshrc

- `echo 'export JAVA_HOME="/Library/Java/JavaVirtualMachines/zulu-17.jdk/Contents/Home"' >> ~/.zshrc`

### Running Ansible Playbook

> This playbook is not fully unattended due to app Logi Options + requiring password entry to install

`ansible-playbook macOS/mac-os-dev.yml --ask-become-pass`

### Github auth login & final steps

- `gh auth login`
- Finish usual setup of apps which cannot be completed unattended (Logi Options, etc)
