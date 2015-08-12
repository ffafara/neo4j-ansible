# neo4j Ansible Playbooks

Use these playbooks to boot a neo4j development environment using Vagrant.

## Requirements

* Ansible 1.4+
* VirtualBox or VMWare Fusion
* Vagrant

## Usage

* Clone this repo.
* `vagrant up` or `vagrant up --provider=vmware_fusion` if you're using VMware Vagrant.
* Once provisioned, neo4j will be available at `http://192.168.33.10`

That's it.

## Authentication

The default username and password are `username` and `password`.

## Upstart

This playbook uses `upstart` to restart neo4j automatically whenever the server is restarted.

## Licence

The Ansible playbooks are licenced under MIT as described in `LICENCE.md`. neo4j is licenced under GPLv3 as described in [its README](https://github.com/neo4j/neo4j#licensing).

## Contributors

[Sam Knight](https://github.com/samknight)