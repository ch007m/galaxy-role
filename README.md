## Ansible dummy project

Interesting references:

[Import Galaxy role and play with it](https://www.linuxtechi.com/use-ansible-galaxy-roles-ansible-playbook/)
[Create a role and publish it](https://www.opcito.com/blogs/how-to-write-ansible-roles-and-publish-them-on-ansible-galaxy/)

### How to create a galaxy role

Use the `init` command of galaxy to create the skeleton of a role
```bash
ansible-galaxy init role-1
```
Add some tasks as by example `Debug - Say Hello`
Play with the role using a playbook
```bash
ansible-playbook -i hosts hello.yml
```
Add next a git repo and publish it on github

### Install the role from a git hub repo

Install the role using the created github repo
```bash
ansible-galaxy install -r requirements.yml
```
### How To install a galaxy role and use it

To import a galaxy role, execute this command

```bash
$ansenv
ansible-galaxy install bennojoy.ntp
```

Check the information of the role
```bash
ansible-galaxy info bennojoy.ntp
or list it under your home ansible directory
 ls -la $HOME/.ansible/roles/bennojoy.ntp
```

Do a ping using the ntp role
```bash
ansible -m ping -i hosts all
```

Play with the role using a playbook
```bash
ansible-playbook -i hosts ntp.yml
```




