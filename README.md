
# create user with password authentication
add user and with a specific group using ansible playbook
## Installation
1> [setup ansible server and node cluster with ansadmin sudo user using docker container or aws cloud](https://www.google.com)</br>
2> install python3 using [sudo yum install python3 command]

## Usage

```python
susanta@server# ansible-playbook add-user-passwd-auth.yml
password>>
TASK [set passsword] *****************************************************************************************************************
ok: [127.0.0.1]

TASK [set user javascript as a global variable] **************************************************************************************
ok: [127.0.0.1]

TASK [set group django_developer as a global variable] *******************************************************************************
ok: [127.0.0.1]

TASK [debug] *************************************************************************************************************************
ok: [127.0.0.1] => {
    "msg": "$6$TzlqNGZ5wth3.CYb$TRU1Q6XFn26ZphGltGVgUZ6gKWWPERSN7B8bEqzOjukTtCHbJ7PDQlwZxDCWXXAMpNbWrMLRSpCC.MvW7kG4./"
}

PLAY [demo] **************************************************************************************************************************

TASK [Gathering Facts] ***************************************************************************************************************
ok: [node9]

TASK [set user javascript as local scope] ********************************************************************************************
ok: [node9]

TASK [set group django_developer as local scope] *************************************************************************************
ok: [node9]

TASK [debug] *************************************************************************************************************************
ok: [node9] => {
    "hostvars['localhost']['passwd']": "$6$TzlqNGZ5wth3.CYb$TRU1Q6XFn26ZphGltGVgUZ6gKWWPERSN7B8bEqzOjukTtCHbJ7PDQlwZxDCWXXAMpNbWrMLRSpCC.MvW7kG4./"
}

TASK [debug] *************************************************************************************************************************
ok: [node9] => {
    "msg": "$6$TzlqNGZ5wth3.CYb$TRU1Q6XFn26ZphGltGVgUZ6gKWWPERSN7B8bEqzOjukTtCHbJ7PDQlwZxDCWXXAMpNbWrMLRSpCC.MvW7kG4./"
}

TASK [Make sure we have a django_developer group] ************************************************************************************
ok: [node9]

TASK [Allow the group django_developer to have passwordless sudo] ********************************************************************
ok: [node9]

TASK [Creating user {{user_name}} with admin access] *********************************************************************************
changed: [node9]

PLAY RECAP ***************************************************************************************************************************
127.0.0.1                  : ok=6    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node9                      : ok=8    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```
type user password for password authentication

