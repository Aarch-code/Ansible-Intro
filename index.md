
# Ansible: Intro

Ansible is a simple open-source automation engine that simplifies provisioning, configuration management, and deployment of applications. It is available for all popular platforms and is meant to be easy to install and configure.

Ansible playbooks describe automation jobs. They are written using YAML, which is a human-readable data-serialization language. Playbooks contain tasks that are executed on hosts.

We will be installing Ansible Playbook and then the LAMP stack on an Ubuntu server.

LAMP stack is a web service stack that consists of the Linux operating system, the Apache HTTP Server, the MySQL relational database management system, and the PHP programming language.

## Install Ansible

You can use the following commands to install Ansible on Debian-based systems:

* *"sudo apt-get update"
* *"sudo apt-get install ansible"


![image](https://user-images.githubusercontent.com/58585532/156116224-7a947957-376a-4dfc-addc-c6540016e015.png)

![image](https://user-images.githubusercontent.com/58585532/156116336-f0bcc94b-9667-4597-a93d-33204a134c95.png)

## Configure Hosts File

By default, Ansible connects to all remote devices via SSH with the same username that you are using on the control node.
So, in order to actually use Ansible to manage your remote server, you just need to configure the host information.

The default location for the inventory file, containing the Ansible host information, is /etc/ansible/hosts. You can freely add the IP address of the remote server you will be configuring with Ansible, to the end of the file as the actual location in the file is not important. The file itself usually contains just a list of IP and/or domain addresses.

* *"sudo nano /etc/ansible/hosts"

## Install LAMP stack

* *"ansible-playbook <playbook>"

The playbook should install Apache, MySQL, and PHP (the LAMP stack) on server. Keep in mind that the installation might take a minute or two. Once the playbook finishes, you will have a server with the LAMP stack configured on it.

## Confirm Installation

Now that you have successfully installed the LAMP stack to the server with Ansible, it is time to confirm that it actually exists. You can do that by just visiting the server address with a web browser.

_"Open a browser and visit http://<ip address>"_

![image](https://user-images.githubusercontent.com/58585532/156119594-0d157db8-fb9b-4a9c-b6df-47ee5f5751d0.png)

  
  






