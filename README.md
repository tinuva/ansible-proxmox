# ansible-proxmox

This playbook and group of roles are used to configure my proxmox cluster. Some of the setup isn't ideal, but it's a home lab, not on the internet, don't run this in production and so on.


I used this set of commands to test the playbook out on a single proxmox VM. It works, but you'll need to setup your hosts file correctly to run it on a cluster. 

~~~
apt update
apt install git ansible -y
mkdir -p /etc/ansible
echo "[proxmox]" >> /etc/ansible/hosts
echo "localhost ansible_host=127.0.0.1 ansible_user=root" >> /etc/ansible/hosts
git clone https://github.com/tinuva/ansible-proxmox.git
cd ansible-proxmox
ansible-playbook main.yml
~~~

Todo:
* ansible-vault some things
