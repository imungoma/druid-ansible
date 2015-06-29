Ansible Sandbox
===============

ssh_setup
---------
ansible-playbook  --extra-vars="user=ssh_user" --ask-pass -i ./inventories/druid playbooks/add-ssh-key.yml -vvvv

update druid version
-------------------
ansible-playbook -i ./inventories/druid  --sudo-user=some_sudo_user --tags="druid_install,druid_mvn_deps,copy_configs,restart" --limit overload ./playbooks/druid.yml  -vvvv --ask-sudo-pass

druid_deploy
------------
ansible-playbook  -i inventories/druid --sudo-user=some_sudo_user --ask-sudo playbooks/druid.yml -vvvv --ask-sudo-pass
