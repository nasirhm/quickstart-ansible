# Ansible Modules
## Short Intro : 
Ansible modules are reusable, standalone scripts that can be used by the Ansible API, or by the ansible or ansible-playbook programs. They return information to ansible by printing a JSON string to stdout before exiting. They take arguments in one of several ways which we'll go into as we work through this tutorial.

## This repo : 
In this repo I've created my custom module for ansible which gets the http result code of `nasirhussain.tech` and returns it once the playbook is executed.

To Execute : `ansible-playbook main.yml`