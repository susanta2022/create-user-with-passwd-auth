
# create user with password authentication
add user and with a specific group using ansible playbook
## Installation
1> [setup ansible server and node cluster with ansadmin sudo user using docker container or aws cloud](https://www.google.com)</br>
2> install python3 using [sudo yum install python3]</br>
3> create user with proper user group to add-user-passwd-auth.yml like</br>
```python
- hosts: 127.0.0.1
  connection: local

  vars:
  
    user_name: username
    group: user_group_name
    
  tasks:
```

## Usage

```python
susanta@server# ansible-playbook add-user-passwd-auth.yml
password>>

PLAY RECAP ***************************************************************************************************************************
127.0.0.1                  : ok=6    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node9                      : ok=8    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
type user password for password authentication

