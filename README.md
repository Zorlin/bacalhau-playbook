
bacalhau-playbook
=================

Bacalhau on autopilot. Aims to make setting up, upgrading, maintaining and troubleshooting Bacalhau clients, nodes and clusters a breeze.

Supports less systems than the original Bacalhau installer, we'll fix that over time. Quick 'n dirty for now.

Getting started
===============

Clone this repository somewhere handy
* git clone https://github.com/Zorlin/bacalhau-playbook.git

Generate an SSH key if you don't already have one
* ssh-keygen

Copy your key to all the boxes you want to manage (replace localhost with the machine you want)
* ssh-copy-id localhost

Edit the inventory file as appropriate. Copy vars/settings.yml.dist to vars/settings.yml and save a copy of your settings somewhere safe after editing them to suit your needs.

Install the required roles, and do an Ansible run.

ansible-galaxy install -r roles/requirements.yml && ansible-playbook site.yml

Inventories
===========
Here are a list of included inventories.

* inventory is for testing purposes.

Roadmap
=======
Nothing yet, sorry

Credits
=======
Developed in 2023 by [Benjamin Arntzen](https://github.com/Zorlin) and [Protocol Labs](https://protocol.ai) with assistance and kindness from the Bacalhau Project team and contributors. <3