<<<<<<< HEAD
wp-emerson
Instalando wordpress com ansible
Utilizado CentOS 7
Instale ansible
#yum install ansible -y

No diretório /etc/ansible faça o clone do repositório, diretórios /playbooks e /roles mantenha na raíz do diretório, a instalação foi feita em localhost edite o arquivo de inventário hosts.
=======
# wp-emerson
## Instalando wordpress com ansible

## Utilizado CentOS 7 ##

# Instale ansible 

#yum install ansible -y

No diretório /etc/ansible faça o clone do repositório, diretórios /playbooks e /roles mantenha na raíz do diretório, a instalação foi feita em localhost edite o arquivo de inventário hosts. 
>>>>>>> 48630fdc6352fdf6109fad14409f1be274494f58

#vim hosts

[wordpress]

127.0.0.1

<<<<<<< HEAD
Para testar comunicação do host
#ansible localhost -c local -i hosts -m ping

Executar o arquivo #playbook.yml que se encontra no diretório /playbooks
=======
## Para testar comunicação do host

#ansible localhost -c local -i hosts -m ping

## Executar o arquivo #playbook.yml que se encontra no diretório /playbooks

>>>>>>> 48630fdc6352fdf6109fad14409f1be274494f58
#ansible-playbook -c local -i hosts playbooks/playbook.yml
