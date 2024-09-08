<img src="./resources/ansible-logo.png" alt="Ansible" width="100"/>

### Install Ansible

```shell
sudo apt install ansible-core

ansible-vault encrypt vault.yml

ansible-playbook -i inventory.ini playbook__debian__workstation-setup.yml --ask-vault-pass -vv

# Vault.yml password: 123
```

### Oracle Client installation step

```shell
sudo mkdir /opt/oracle

wget https://download.oracle.com/otn_software/linux/instantclient/2115000/instantclient-basic-linux.x64-21.15.0.0.0dbru.zip -P /opt/oracle/

sudo unzip /opt/oracle/instantclient-basic-linux.x64-21.15.0.0.0dbru.zip

sudo sh -c "echo export LD_LIBRARY_PATH=/opt/oracle/instantclient_21_15:$LD_LIBRARY_PATH >> ~/.bashrc"

sudo sh -c "echo export ORACLE_HOME=/opt/oracle/instantclient_21_15:$PATH >> ~/.bashrc"

sudo source ~/.bashrc

sudo ln -s /usr/lib/x86_64-linux-gnu/libaio.so.1t64 /opt/oracle/instantclient_21_15/libaio.so.1

sudo sh -c "echo /opt/oracle/instantclient_21_15 > /etc/ld.so.conf.d/oracle-instantclient.conf"

sudo ldconfig
```
