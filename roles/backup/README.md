Role Name
=========

pfSense backup role creator

Requirements
------------

Case you want, change the backup destination otherwise it will be stored on /ansible/pfsense/roles/backup/files

Role Variables
--------------

The role is using vars present on group_vars/pfsense

Dependencies
------------

There's no dependencies to this role

Example Playbook
----------------

All roles are comment, to use backup role, configure /roles/backup/tasks/main.yml 

# pfsense playbook

- name: pfSense 2.4.4 Playbook
  hosts: pfsense
  roles:
   - backup
   #- alias
   #- rule
   #- update
   #- common

License
-------

BSD

Author Information
------------------

by 5h0ckw4v3
