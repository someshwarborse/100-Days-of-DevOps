# Day 2 - Advanced Linux

📅 Day 2 - User & Permission Management in Linux
🔹 1. User Management
Created a new user: sudo useradd devopsuser

Set a password: sudo passwd devopsuser

Modified user home directory: sudo usermod -d /home/newhome devopsuser

Deleted a user: sudo userdel -r devopsuser

🔹 2. Group Management
Created a group: sudo groupadd devops

Added a user to a group: sudo usermod -aG devops devopsuser

Checked user groups: groups devopsuser

Deleted a group: sudo groupdel devops

🔹 3. File & Directory Permissions
Checked file permissions: ls -l file.txt

Changed file permissions: chmod 700 script.sh

Changed file owner: sudo chown devopsuser file.txt

Changed file group: sudo chgrp devops file.txt

✅ Key Learnings
Linux uses users and groups to manage access control.

Permissions (r, w, x) define what a user can do with a file.

chown and chmod help in securing files in a multi-user environment.
