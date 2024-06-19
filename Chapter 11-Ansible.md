## Ansible
Ansible configuration primarily happens through an INI-style file named `ansible.cfg`. This file defines various settings for Ansible's behavior. Here's a basic overview of what you might find in this file:

* **Inventory:** This section defines the location of your inventory file, which lists the systems Ansible manages (e.g., `inventory = /etc/ansible/hosts`).
* **Connection:** This section specifies how Ansible connects to managed systems. The default is typically `smart` which gathers facts about the system intelligently.
* **Credentials:** You can define default credentials like the `sudo_user` for privileged tasks.
* **Paths:** Ansible uses various plugins for modules, callbacks, etc. This section defines search paths for these plugins.
* **Logging:** You can enable logging by specifying a `log_path`.

**Important points:**

* The default configuration file is usually `/etc/ansible/ansible.cfg`. However, Ansible searches for the file in several locations including your current directory. 
* Most basic configurations can be overridden using command-line flags or within playbooks themselves.

It's recommended to keep the default configuration for starters and customize it as needed for your specific environment.

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
