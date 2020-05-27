# Ansible Windows Devlopment

This will help you setup Windows development environment.  I use it for testing Ansible playbooks and various other scripts.

## Requirements

- Vagrant
- Ansible
- Packer (If you are creating your own boxes)

## Getting started

You will need to run the `setup.yml` playbook with Ansible.  There are a few core variables that will need to be defined in order to make things easier.

## Creating the Vagrant base boxes

If you wish to create your own boxes, you can run the `packer-setup.yml` playbook with Ansible.  You will have to pass a variable to build the version you want.

Version available are

- 2012
- 2012r2
- 2016
- 2019

### Import the images

After creating each of the base boxes, you will have to import them for Vagrant to use.  You will need to have a namespace defined.
