Role Name
=========

pfSense update role

Requirements
------------

change packages that will be updated in ./tasks/main.yml

Role Variables
--------------

The role is using vars present on group_vars/pfsense

Dependencies
------------

There's no dependencies to this role

Example Playbook
----------------

All roles are comment, to use update role first check the package that will updates and change /roles/update/tasks/main.yml
in according your needs this role will allow you update or install any package you want to get the correctly package name
connect in you pfsense and run: sudo pkg search package_name and then use it to install for all you instances bellow an example
for zabbix package options

sudo pkg search zabbix
pfSense-pkg-zabbix-agent-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-agent22-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-agent32-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-agent34-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-agent4-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-agent42-1.0.4 pfSense package zabbix-agent
pfSense-pkg-zabbix-proxy-1.0.4 pfSense package zabbix-proxy
pfSense-pkg-zabbix-proxy22-1.0.4 pfSense package zabbix-proxy
pfSense-pkg-zabbix-proxy32-1.0.4 pfSense package zabbix-proxy
pfSense-pkg-zabbix-proxy34-1.0.4 pfSense package zabbix-proxy
pfSense-pkg-zabbix-proxy4-1.0.4 pfSense package zabbix-proxy
pfSense-pkg-zabbix-proxy42-1.0.4 pfSense package zabbix-proxy
zabbix22-agent-2.2.21_1        Enterprise-class open source distributed monitoring (agent) LTS
zabbix22-proxy-2.2.21_1        Enterprise-class open source distributed monitoring (proxy) LTS
zabbix3-agent-3.0.16           Enterprise-class open source distributed monitoring (agent) LTS
zabbix3-proxy-3.0.16           Enterprise-class open source distributed monitoring (proxy) LTS
zabbix32-agent-3.2.11_1        Enterprise-class open source distributed monitoring (agent)
zabbix32-proxy-3.2.11_1        Enterprise-class open source distributed monitoring (proxy)
zabbix34-agent-3.4.8           Enterprise-class open source distributed monitoring (agent)
zabbix34-proxy-3.4.8           Enterprise-class open source distributed monitoring (proxy)
zabbix4-agent-4.0.0            Enterprise-class open source distributed monitoring (agent) LTS
zabbix4-proxy-4.0.0            Enterprise-class open source distributed monitoring (proxy) LTS
zabbix42-agent-4.2.1           Enterprise-class open source distributed monitoring (agent)
zabbix42-proxy-4.2.1           Enterprise-class open source distributed monitoring (proxy)

then I could choose pfSense-pkg-zabbix-proxy42 to install or update e change update role like bellow 

- name: pfSense zabbix-proxy install
  shell: pkg remove -y pfSense-pkg-zabbix-proxy42

So I could uncomment update on pfsense.yml and would be possible install zabbix proxy pacakge to all my pfsense instances present
on group hosts on my inventory file in this playbook called hosts

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
