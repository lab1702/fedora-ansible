# fedora-ansible

TODO: Update from Ubuntu to Fedora specifics.

Ansible configuration that can be used with Fedora Workstation.

## Complete Workstation Setup

### Option 1: Ansible Commands for non-root users

#### Run this once after installing the OS

    sudo apt update && sudo apt upgrade -y && sudo apt install -y git ansible

#### Run this to apply the config to your workstation

    sudo ansible-pull -U https://github.com/lab1702/ubuntu-ansible.git

#### Run this if you don't want to have to sudo docker commands

    sudo usermod -aG docker $USER

## OpenCode

    curl -fsSL https://opencode.ai/install | bash

## Rust

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

## NodeJS

*This is needed if you want to install Artillery, Claude Code, Gemini CLI and other npm packages.*

### Configure npm to install packages in user home directory

    mkdir ~/.npm-global
    npm config set prefix '~/.npm-global'
    echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc
    export PATH=~/.npm-global/bin:$PATH

## Artillery Load Tester

    npm install -g artillery@latest

## Claude Code

    npm install -g @anthropic-ai/claude-code
