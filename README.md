# Mac Development Ansible Playbook

![Ansible Playbook Logo](files/Mac-Dev-Playbook-Logo.png)

[![CI][badge-gh-actions]][link-gh-actions]

[![MegaLinter](https://github.com/javydekoning/mac-dev-playbook/workflows/MegaLinter/badge.svg?branch=main)](https://github.com/javydekoning/mac-dev-playbook/actions?query=workflow%3AMegaLinter+branch%3Amain)

This playbook installs and configures most of the software I use on my Mac for web and software development. Some things in macOS are slightly difficult to automate, so I still have a few manual installation steps, but at least it's all documented here.

## Installation

  1. Ensure Apple's command line tools are installed (`xcode-select --install` to launch the installer).
  2. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html):

     1. Run the following command to add Python 3 to your $PATH: `export PATH="$HOME/Library/Python/3.9/bin:/opt/homebrew/bin:$PATH"`
     2. Upgrade Pip: `sudo pip3 install --upgrade pip`
     3. Install Ansible: `pip3 install ansible`

  3. Clone or download this repository to your local drive.
  4. Run `ansible-galaxy install -r requirements.yml` inside this directory to install required Ansible roles.
  5. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your macOS account password when prompted for the 'BECOME' password.

## Author

This project was modified by [Javy de Koning](https://www.javydekoning.com/), forked from
[Jeff Geerling](https://www.jeffgeerling.com/).

[badge-gh-actions]: https://github.com/javydekoning/mac-dev-playbook/workflows/CI/badge.svg?event=push
[link-gh-actions]: https://github.com/javydekoning/mac-dev-playbook/actions?query=workflow%3ACI
