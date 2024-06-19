## Ansible

11.1 Ansible Basics
Needed to run Anssible smoothly:
* run SSH commands
* configure client SSH keys
* configure host SSH keys
Ansible calculates the commands on the server and sends simple commands as the control machine  
Install Ansible in virtual enviroment:
```python
ip install ansible
```
Verify that is there, so ping the localhost
```bash
$ ansible localhost -m ping
```
