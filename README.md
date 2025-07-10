-------------------
To connect vscode
-------------------
Ctrl+shif+P

[Command]
Remote-SSH: Connect to Host

-------------------
Run playbook
-------------------
Option 1: Will use user and password defined in inventory file (not ideal to store password in files)

ansible-playbook -i inventory.ini post-pilot-playbook.yml

Option 2: Will prompt for password (more secured)

ansible-playbook -i inventory.ini -u admin --ask-pass post-pilot-playbook.yml

Option 3: make user sudo
ansible-playbook -i inventory.ini -u admin --ask-become-pass post-pilot-playbook.yml