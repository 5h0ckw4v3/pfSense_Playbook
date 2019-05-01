Role Name
=========

pfSense role rules creator

Requirements
------------

change the alias name in /roles/rules/tasks/main.yml
this part of shell command `ifconfig vmx0 | grep inet | grep -v inet6 | awk '{print $2}' | cut -d"." -f1-3`.0/24 must be changed.
Where's vmx0 you must change with you pfsense lan nic name, so to use that you need to have a name standard on all you pfSense
instances and put always the same nic name as you lan network and then you will be able to create rule for some destination from
each lan network present on your pfSense intances.

E.g cause you vmx0 has an IP from 192.168.1.0/24 network so.
`ifconfig vmx0 | grep inet | grep -v inet6 | awk '{print $2}' | cut -d"." -f1-3`.0/24 = 192.168.1.0/24

so this {easyrule pass lan any `ifconfig vmx0 | grep inet | grep -v inet6 | awk '{print $2}' | cut -d"." -f1-3`.0/24 any}
is equal that {easyrule pass lan any 192.168.1.0/24 any} so using like this ansible will be able to apply a different rule for each
pfSense instance based on ip has set up on lan nic in this E.g vmx0


Role Variables
--------------

The role is using vars present on group_vars/pfsense

Dependencies
------------

There's no dependencies to this role

Example Playbook
----------------

All roles are comment, to use rules role in rules/task/main.yml by your needs.

# pfsense playbook

- name: pfSense 2.4.4 Playbook
  hosts: pfsense
  roles:
  
   #- backup
   
   #- alias
   
   #- rule
   
    - update
    
   #- common

License
-------

BSD

Author Information
------------------

by 5h0ckw4v3
