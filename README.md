###Ansible Playbooks for Laravel 5

This installs the following software on your standard Linux.

* php7 with batteries
* nginx
* git
* composer
* memcached

##### Requirements

* python 2.7 must be installed on your machine
* linux instance (e.g. ubuntu/images/hvm-ssd/ubuntu-xenial-16.04-amd64-server-20160610 (ami-0ae77879))

##### Brief

Ideally suitable for Laravel setups, this Ansible provision recipe does a lot more than you might think. The nginx configuration includes the industry standard optmizations so you can run a high traffic site out of the box. 

The php7.0 'batteries included' build by Ondrej Sury comes with all the necessary extensions to satisfy major framework requirements. This includes curl, fpm, mysql, gd, mbstring, mcrypt, memcached etc.

##### Ansible

Ansible is a great tool for provisioning servers using an agentless form. So you can do the following:

1. Use a vagrant box on your local machine and control your fleet of servers.
2. Use a t2.micro instance on Amazon and use it to control your fleet of servers.

I would recommend this(https://serversforhackers.com/video/ansible-installation-and-basics) guide to install Ansible.

##### Running

Running this is as simple as executing the following command from the `/roles/` directory:

`ansible-playbook --private-key=~/.ssh/your-web-server.pem provision.yml`