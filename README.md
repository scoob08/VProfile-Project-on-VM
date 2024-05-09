# VPROFILE PROJECT

## Project Summary

The VPROFILE project is a comprehensive setup guide for deploying a web application stack using Vagrant, Virtualbox, and various software components like Nginx, Tomcat, RabbitMQ, Memcache, and MySQL. The project aims to provide a seamless setup process for developers to create a development environment quickly.

The setup process involves cloning the source code, provisioning virtual machines, setting up services like web servers, application servers, message brokers, and databases in a specific order. Each component's setup includes steps for VM setup, software installation, configuration, and firewall setup.

The project's key components include:
- **Prerequisites:** Oracle VM Virtualbox, Vagrant, and Git bash are required.
- **VM Setup:** Involves cloning the source code, switching to the main branch, and bringing up VMs using Vagrant.
- **Provisioning Services:** Sets up essential services like Nginx, Tomcat, RabbitMQ, Memcache, and MySQL.
- **MySQL Setup:** Covers installation, securing, and initializing MySQL database.
- **Memcache Setup:** Covers installation and configuration of Memcache for database caching.
- **RabbitMQ Setup:** Covers installation, user setup, and firewall configuration for RabbitMQ.
- **Tomcat Setup:** Covers installation, configuration, and deployment of Tomcat application server.
- **Code Build & Deploy:** Guides through building and deploying the application code.
- **Nginx Setup:** Covers installation, configuration, and setup of Nginx as a reverse proxy.

Overall, the VPROFILE project provides a step-by-step guide for setting up a development environment with all necessary components to run a web application efficiently.

---

## Prerequisites
- Oracle VM Virtualbox
- Vagrant
- Vagrant plugins: Execute below command in your computer to install hostmanager plugin
- Git bash or equivalent editor

## VM SETUP
1. Clone source code.
2. Cd into the repository.
3. Switch to the main branch.
4. cd into `vagrant/Manual_provisioning`.
5. Bring up vm’s
- NOTE: Bringing up all the vm’s may take a long time based on various factors. If vm setup stops in the middle run `vagrant up` command again.
- INFO: All the vm’s hostname and `/etc/hosts` file entries will be automatically updated.

...


# VPROFILE PROJECT SETUP

## Prerequisites
- Oracle VM Virtualbox
- Vagrant
- Vagrant plugins: Execute below command in your computer to install hostmanager plugin
- Git bash or equivalent editor

## VM SETUP
1. Clone source code.
2. Cd into the repository.
3. Switch to the main branch.
4. cd into `vagrant/Manual_provisioning`.
5. Bring up vm’s
- NOTE: Bringing up all the vm’s may take a long time based on various factors. If vm setup stops in the middle run `vagrant up` command again.
- INFO: All the vm’s hostname and `/etc/hosts` file entries will be automatically updated.

## PROVISIONING Services
1. **Nginx** => Web Service
2. **Tomcat** => Application Server
3. **RabbitMQ** => Broker/Queuing Agent
4. **Memcache** => DB Caching
5. **ElasticSearch** => Indexing/Search service
6. **MySQL** => SQL Database Setup should be done in below mentioned order:
- MySQL (Database SVC)
- Memcache (DB Caching SVC)
- RabbitMQ (Broker/Queue SVC)
- Tomcat (Application SVC)
- Nginx (Web SVC)

## MYSQL SETUP
1. Login to the db vm
2. Verify Hosts entry, if entries missing update it with IP and hostnames
3. Update OS with latest patches
4. Set Repository
5. Install Maria DB Package
6. Starting & enabling mariadb-server
7. Run mysql secure installation script.
- NOTE: Set db root password, I will be using `admin123` as password
- Follow the prompts to secure the installation.

## MEMCACHE SETUP
...

## RABBITMQ SETUP
...

## TOMCAT SETUP
...

## CODE BUILD & DEPLOY (app01)
...

## NGINX SETUP
...
