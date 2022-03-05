# DevOpsAnsibleProject2

* This is project 2 in course 2 of the CalTech DevOps post-graduate certificate program
* The objective of this project is to deploy a wordpress site on a target server using an ansible playbook

## Problem Space

---

### DESCRIPTION

You are a DevOps engineer at XYZ Ltd. Your company is working mostly on WordPress projects. A lot of development hours are lost to perform WordPress setup with all dependencies like PHP, MySQL, etc. The Company wants to automate it with the help of a configuration management tool so that they can follow a standard installation procedure for WordPress and its components whenever a new requirement or client comes in. The below mentioned components should be included:

- PHP
- Nginx/Apache Web Server
- MySQL
- WordPress
 

Steps to Perform:

- Establish configuration management master connectivity with WordPress server
- Validate connectivity from master to slave machine
- Prepare IaaC scripts to install WordPress and its dependent components
- Execute scripts to perform installation of complete WordPress environment
- Validate installation using the public IP of VM by accessing WordPress application

## System Configuration

---

### Environemnt 

* 2 Ubuntu 20.04.3 LTS VMs running on HyperV hypervisor
  * ansible-controller (192.168.1.140)
  * ansible-target (192.168.1.139)
    - Snapshot created after system initalization after ssh is enabled. This allows me to quickly revert the target for testing.
  * Personal repository hosted at https://github.com/RedOneLima/DevOpsAnsibleProject2
  * Host(s) Entires added to `C:\Windows\System32\drivers\etc\hosts`

## Playbook description

* Installs the nessisary packages using apt
* Installs the nessisary PHP Extentions
* Sets up Apache2 server
* Sets up MySQL database
* Configures Wordpress install
* Configures Firewall

## Create Web Server

* First, exchange ssh keys with the desired host(s)

```bash

```
