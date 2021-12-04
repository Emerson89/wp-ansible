# Installing wordpress with ansible

## Dependencies
![Badge](https://img.shields.io/badge/CentOS-7-blue)
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)
![Badge](https://img.shields.io/badge/docker-20.10-blue)


# Tests

- Dockerfilecentos 7 for tests, to run use the script build_centos.sh
```
bash build_centos.sh
```
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
```
```
ansible-playbook -i hosts playbook.yml
```
## License
![Badge](https://img.shields.io/badge/license-GPLv3-green)

