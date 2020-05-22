# packer-windows

This repo will create the initial setup to create Packer files to create Windows templates to use with Vagrant.

Each image is built to include:

- Fully updated
- Enable WinRM HTTPS and HTTP listeners
- Enable RDP
- Reset the evaluation timer

## Requirements

These will need to be installed in order to use this.

Linux

- Packer
- Ansible
- pywinrm

Windows

- Packer
- Windows Subsystem for Linux (WSL)
  - Ansible
  - pywinrm

One of the following hypervisors:

- Virtualbox

## How to use

Create packer build files.  This will create folders for each build of Windows.

```
ansible-playbook setup.yml

```

## Variables

```
packer_win_username: vagrant
packer_win_password: vagrant

packer_win_update_category:
    - SecurityUpdates
    - CriticalUpdates
    - Updates
    - UpdateRollups
    - ServicePacks
packer_win_update_loop: 5

```