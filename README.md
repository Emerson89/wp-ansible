# wp-emerson

# Instalando wordpress com ansible

## Utilizado CentOS 7 ##

# Instale ansible 

#yum install ansible -y

# Faça o clone do repositorio

#git clone https://github.com/Emerson89/wp-emerson.git

# Copie os diretorios /playbooks e /roles para o diretorio /etc/ansible, a instalacao foi feita em localhost edite o arquivo de inventorio hosts. 

#cp -r wp-emerson/roles wp-emerson/playbooks /etc/ansible

#vim hosts

[wordpress]

127.0.0.1

# Para testar comunicacao do host

#ansible localhost -c local -m ping

## Executar o arquivo #playbook.yml que se encontra no diretorio /playbooks

#ansible-playbook -c local playbooks/playbook.yml
