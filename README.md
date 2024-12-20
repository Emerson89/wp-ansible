# Installing wordpress with ansible

## Dependencies
- ansible 2.12.0

# Supports SOs
- CentOs 7
- Rocky 8

# Example playbook

```yaml
- name: Applying installation and dependency 
  hosts: all
  vars:
    wp_mysql_db: MyWP
    wp_mysql_user: wpUser
    wp_mysql_password: worddb
  become: yes 
   
  roles:
     - server
```
## Variables
| Name | Description | Default | 
|------|-----------|---------|
| wp_mysql_db | Name database | MyWP|
| wp_mysql_user | Name User database | wpUser | 
| wp_mysql_password | password database | worddb

For local ansible test can be used vagrant

# Edit inventory file

# To test host communication
```
ansible localhost -m ping
ansible localhost -m setup | grep ansible_distribution_major_version
```
```
ansible-playbook -i hosts playbook.yml
```
## License
![Badge](https://img.shields.io/badge/license-GPLv3-green)