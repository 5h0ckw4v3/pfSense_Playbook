# pfSense_Playbook

By now pfSense2.4.4-p2 there's no way to make easy the management an environment with a lot of pfSense instances, but it's possible manage some tasks by terminal like create alias, rules, backups and packages/system update, so I've built this very basic ansible playbook to run these activities in a easiest way using Ansible.

To be able to use this playbook follow steps bellow;
  
  - create administrator user or give all ssh privileges to this user
  - install sudo package on pfsense
  - On system/sudo select this user, run as select User: root, select checkbox No password, and on Command list type ALL.
  - On custom configuration set up to Include at End and Save.
  
  Obs: Avoid to use defaul user Admin if you use him this playbook may does not works as you want.
  
 
