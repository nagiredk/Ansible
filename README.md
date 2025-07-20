##🔒 Create an Ansible Vault
  ansible-vault create vault.yml
When prompted, set a strong vault password. This will encrypt your secrets file.

Example:
[root@vm-ansible-lab ansible]# ansible-vault create vault.yml
New Vault password:

Inside the vault file, add your sensitive variables, for example:
ansible_user: azureuser
ansible_password: Bird@01012025

✅ Update credentials in the Vault
To edit the Vault later:
ansible-vault edit vault.yml


🔍 Test with an Ad-Hoc Command using Vault
Run an ad-hoc ping test with the Vault secrets:
ansible all -i hosts -m ping -e "@vault.yml" --ask-vault-pass

You will be prompted for your Vault password.
I
## ✅ Successful Ansible Ping Test
![Ansible Ping Success](https://raw.githubusercontent.com/nagiredk/IAMNKR/ansible/ansible-azure-rehel-vm/Ansible%20Ping%20Success.png)




