# terraform_ansible_01
A sample project containing my test work using terraform and ansible, with some optional shell-based setups.

#EPJ Ansible Control Box Test

Step 1: Create a control box in aws. (Standard amazon ubuntu)

Create an "ansible target" box in aws. (Standard amazon ubuntu)

Step 2: Log in to the control box, get a shell script that upgrades the system and sets up ansible.

```
wget -O /home/ubuntu/setupansible.sh "http://[domain]/adamd/epjansible/setupansible.sh"
sudo chmod 777 /home/ubuntu/setupansible.sh
sudo bash /home/ubuntu/setupansible.sh
sudo rm /home/ubuntu/setupansible.sh
```

Step 3: Download the ansible playbook.

```
wget -O /home/ubuntu/adamdtest_remote1.zip "http://[domain]/adamd/epjansible/adamdtest_remote1.zip"
unzip /home/ubuntu/adamdtest_remote1.zip
cd adamdtest_remote1
```

Step 4: Modify the hosts file so that it contains the right ip address

Step 5: Run the ansible playbook to provision the "ansible target" server

```
ansible-playbook adamdmicro apache.yml
```

Step 6: Edit your local "hosts" file so that it points [domain name] to the ansible target box's IP address

Step 7:

Browse: http://[domain name]/
