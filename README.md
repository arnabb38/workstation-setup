### Install Ansible

```shell
sudo apt install ansible-core

ansible-vault encrypt vault.yml

ansible-playbook -i inventory.ini playbook__debian__workspace-setup.yml --ask-vault-pass -vv

# Vault.yml password: 123
```
