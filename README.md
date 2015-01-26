Ansible Sandbox
===============

ssh_setup
---------
ansible-playbook  --extra-vars="user=isaac" --ask-pass -i ./inventories/druid playbooks/add-ssh-key.yml -vvvv

druid_deploy
------------
ansible-playbook  -i inventories/druid --sudo-user=root --ask-sudo playbooks/druid.yml -vvvv
