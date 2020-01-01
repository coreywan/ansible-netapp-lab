# Ansible Netapp Lab Repo

Supplemental content to go from zero to hero in the sandbox lab quickly. Great to show an overall solution in the lab for DEMO.

## Setup Jumphost

1. Open Terminal and setup the configuration of the environment
```sh
cd /home/student/Projects
rm -rf ansible-netapp-lab
git clone https://gitlab-cloud.wwtatc.com/atc-demos/ansible-netapp-lab.git
cd ansible-netapp-lab
ansible-galaxy install -r ./roles/requirements.yml -p ./roles
ansible-playbook pb-tower-config-management.yml
```

## Inventories

### POC Inventory

Location: `./inventories/poc/`
Description: To be used for managing the host inventory for the POC environment. At the time of writing this, it just contains the Tower host, and the variables in the inventory to support the configuration of the Tower Instance.

## Playbooks

### pb-tower-config-management.yml

Description: This Playbook is used to help maintain the configuration of the Human POC Tower Instance.
Usage: `ansible-playbook pb-tower-config-management.yml`

### pb-hello-world.yml

Description: A generic playbook to test Tower functionality and also used to test the Service-Now to Ansible Integration.

### pb-test-infrastructure

Description: This is used to test connectivity within the lab environment

Use: `ansible-playbook pb-test-infrastructure.yml`