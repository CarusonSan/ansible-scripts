# ansible-scripts

## macOS Dev Environment

### Prerequisites
1. Install Developer Tools (Python 3.9):
  - `xcode-select --install`
2. Configure Python/pip & install Ansible:
  - `python3 -m pip install --upgrade pip`
  - `python3 -m pip install --user ansible`
  - `nano ~/.zshrc`
  - `export PATH="$HOME/Library/Python/3.9/bin:$PATH"`
3. Run Ansible Playbook:
  - `ansible-playbook macOS/mac-os-dev.yml --ask-become-pass`
