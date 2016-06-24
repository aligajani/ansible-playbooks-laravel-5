###Ansible Playbooks for Laravel 5

This installs the following software on your standard Linux.

* php7 with batteries
* nginx
* git
* composer
* memcached

##### Requirements 

* python 2.7 must be installed on your server [A]
* ansible must be installed from where you are executing playbooks
* linux instance (e.g. ubuntu/images/hvm-ssd/ubuntu-xenial-16.04-amd64-server-20160610 (ami-0ae77879))

##### Brief

Ideally suitable for Laravel setups, this Ansible provision recipe does a lot more than you might think. The configurations includes the industry standard optmizations so you can run a high traffic site out of the box. 

The php7.0 'batteries included' build by Ondrej Sury comes with all the necessary extensions to satisfy major framework requirements. See the list below to marvel at the range of goodies.


* php7.0-common
* php7.0-cli
* php7.0-intl
* php7.0-curl
* php7.0-cgi
* php7.0-fpm
* php7.0-mysql
* php7.0-gd
* php7.0-mbstring
* php7.0-mcrypt
* php7.0-memcached
* php7.0-apcu [B]

##### Ansible

Ansible is a great tool for provisioning servers using an agentless form. So you can do the following:

1. Use a vagrant box on your local machine and control your fleet of servers.
2. Use a t2.micro instance on Amazon and use it to control your fleet of servers.

I would recommend [this](https://serversforhackers.com/video/ansible-installation-and-basics) guide to install Ansible.

##### Running

Running this is as simple as executing the following command from the `ansible-playbooks-laravel-5/` directory:

`ansible-playbook --private-key=~/.ssh/your-web-server.pem provision.yml`

##### Apendices

###### A | _You can do this easily by running `sudo apt-get update` and then `sudo apt-get install python`_.

###### B | _APCU is included to make Opcode caching even better. Opcode comes with PHP 7 built-in by default_.
