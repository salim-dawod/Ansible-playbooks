

To Deploy the playbooks correctly, you should Edit {{hosts}} file in each directory (Offline and Online) based on your remote IP server.

Also you should generate Public and private Key on your host(ansible node controller),
and copy the public key into remote servers 
Example: ssh-copy-id  username@127.0.0.1


To Deploy the playbooks Run these commands in row:
// Change --user and -extra variables as your remote servers:

ansible-playbook -i hosts edit-sysreq-playbook.yaml --user salim -e "username=salim" -vvv

ansible-playbook -i hosts docker-playbook.yaml --user salim -e "username=salim" -vvv

ansible-playbook -i hosts tools-playbook.yaml --user salim -e "username=salim" -vvv

