Role Name
=========

pfSense alias creator

Requirements
------------

change the alias name in ./file/alias.txt

Role Variables
--------------

The role is using vars present on group_vars/pfsense

Dependencies
------------

There's no dependencies to this role

Example Playbook
----------------

All roles are comment, to use alias role configure ./file/alias.txt and alias/task/main.yml by your needs.

# pfsense playbook

- name: pfSense 2.4.4 Playbook
  hosts: pfsense
  roles:
  
   #- backup
   
   - alias
   
   #- rule
   
   #- update
   
   #- common

License
-------

BSD

Author Information
------------------

by 5h0ckw4v3
