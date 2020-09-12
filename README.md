# Installing wordpress with ansible

## Dependências
![Badge](https://img.shields.io/badge/CentOS-7-blue)
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)

# Edit inventory file

# To test host communication
```
ansible localhost -m ping
```

## Playbook example
```
---
- name: Install wordpress
  hosts: all
  become: yes
  roles:
  - server
  - php
  - mysql
  - wordpress
```
ansible-playbook -i hosts playbook.yml
```
## License
![Badge](https://img.shields.io/badge/license-GPLv3-green)

