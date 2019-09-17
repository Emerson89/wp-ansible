# wp-emerson
Instalando wordpress com ansible

## Utilizado CentOS 7 ##

# Instale ansible 

yum install ansible -y

#No diretório /etc/ansible faça o clone do repositório, diretórios /playbooks, /roles mantenha na raíz do diretório, a instalação foi feita em localhost edite o arquivo de inventário hosts. 

[wordpress]
127.0.0.1

## Para testar comunicação do host

ansible localhost -c local -i hosts -m ping

## Executar o arquivo #playbook.yml que se encontra no diretório /playbooks

ansible-playbook -c local -i hosts playbooks/playbook.yml
