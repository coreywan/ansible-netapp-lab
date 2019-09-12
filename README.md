# Ansible Netapp Lab Repo

Supplemental content to go from zero to hero in the sandbox lab quickly. Great to show an overall solution in the lab for DEMO.

## Inventories

### POC Inventory

Location: `./inventories/poc/`
Description: To be used for managing the host inventory for the POC environment. At the time of writing this, it just contains the Tower host, and the variables in the inventory to support the configuration of the Tower Instance.

## Playbooks

### pb-tower-config-management.yml

Description: This Playbook is used to help maintain the configuration of the Human POC Tower Instance.
Usage: `ansible-playbook  --ask-vault-pass -i inventories/poc/hosts pb-tower-config-management.yml`

### pb-hello-world.yml

Description: A generic playbook to test Tower functionality and also used to test the Service-Now to Ansible Integration.


### Temporary Docs to get everything going

1. Open Terminal
```sh
cd /home/student/Projects
rmdir ansible-netapp-lab
git clone https://github.com/coreywan/ansible-netapp-lab.git
cd ansible-netapp-lab
ansible-galaxy install -r ./roles/requirements.yml -p ./roles
ansible-playbook  --ask-vault-pass -i inventories/poc/hosts pb-tower-config-management.yml

```