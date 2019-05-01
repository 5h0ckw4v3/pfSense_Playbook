# pfSense_Playbook

By now pfSense2.4.4-p2 there's no way to make easy the management an environment with a lot of pfSense instances, but it's possible manage some tasks by terminal like create alias, rules, backups and packages/system update, so I've built this very basic ansible playbook to run these activities in a easiest way using Ansible.

To be able to use this playbook follow steps bellow;
  
  - create administrator user or give all ssh privileges to this user
  
  - install sudo package on pfsense
  
  - On system/sudo set it up like bellow;
      - select this user
      - run as select User: root
      - select checkbox No password
      - In Command list box type ALL
      
  - On custom configuration set up to Include at End and Save.
  
Obs: Avoid to use defaul user Admin if you use him this playbook may does not works as you want.

To learn how to use this playbook read readme's roles, each role has its own readme with instructions to create backup, alias, rules and to update packages and system.

Case you are starting from scratch with ansible, bellow some steps to you set ansible up on centOS7 and then after that you will be able to run this playbook (edited by you before, of course).
  
  centOS 7
  -
  
  - sudo yum install epel-release -y
  - sudo yum update -y
  - sudo yum install ansible -y
  - git clone https://github.com/5h0ckw4v3/pfSense_Playbook.git
  - cd pfSense_Playbook
  - cp ansible_config/.vimrc /home/your_user
  - sudo mv /etc/ansible/ansible.cfg /etc/ansible/ansible_old.cfg
  - sudo cp ansible_config/ansible.cfg /etc/ansible/

5h0ckw4v3
-
