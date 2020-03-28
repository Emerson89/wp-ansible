# wp-emerson

# Installing wordpress with ansible 2.4.2.0

## Used CentOS 7 ##

# Edit inventory file, installation can be done on localhost.

#vim hosts

[wordpress]

127.0.0.1

# Access the wp-centos directory and execute the commands

# To test host communication

#ansible localhost -m ping

## Run the file # playbook.yml

#ansible-playbook playbook.yml