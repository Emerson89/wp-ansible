# wp-emerson

# Installing wordpress with ansible

## Used CentOS 7 ##

# Install ansible

#yum install ansible -y

# Clone the repository

#git clone https://github.com/Emerson89/wp-emerson.git

# Move the directories / playbooks and / roles to the / etc / ansible directory, the installation was done on localhost and edit the hosts inventory file.

#mv wp-emerson / roles wp-emerson / playbooks / etc / ansible

#vim hosts

[wordpress]

127.0.0.1

# To test host communication

#ansible localhost -c local -m ping

## Run the file # playbook.yml found in the directory / playbooks

#ansible-playbook -c local playbooks / playbook.yml
