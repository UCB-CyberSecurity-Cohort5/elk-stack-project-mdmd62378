## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.

  - A Load balancer protects the network's integrity through the process of allocating incoming traffic over our network Webservers. The importance of such a feature on a Load Balancer is that we avert a shutdown so that our network constantly remains available.   
  
  - A Jump Box allows remote access to only authorized users through a channel of preselected restrictions to preserve network security. 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the file system of the VMs on the network and system metrics.
  
  - Filebeat: Filebeat is a data shipper that I used for monitoring purposes on my webservers to detect any changes that occurred to the Filesystem of my Virtual Machines.

  - Metricbeat: Metricbeat is a data shipper that I used for monitoring purposes on my webservers to detect any changes that occurred to the system metrics.

The configuration details of each machine may be found below.

| Name     | Function  | IP Address | Operating System |
|----------|-----------|------------|------------------|
| Jump Box | Gateway   | 10.1.0.4   | Linux            |
| Web1     | Webserver | 10.1.0.5   | Linux            |
| Web2     | Webserver | 10.1.0.6   | Linux            |
| Web3     | Webserver | 10.1.0.7   | Linux            |
| Elk      | Webserver | 10.0.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- Public IPv4 IP: 73.202.41.242

Machines within the network can only be accessed by the Jump Box.
- I only allowed SSH access to the Jump Box from my home network machine with an IP Address of 73.202.41.242. 
The Jump Box had authorization to SSH into the Elk Server via the private IP address of 10.1.0.4. 

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box |      Yes            |    73.202.41.242     |
| Web1     |      No             |    10.0.0.4          |
| Web2     |      No             |    10.1.0.4          |
| Web3     |      No             |    10.1.0.4          |
| Elk      |      No             |    10.1.0.4          |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
  
  - The benefit of using an automation tool such as Ansible is that it excels in the efficiency and accuracy of software implementation by expediting the process to install multiple applications in mass deployment rather than individually installing applications.

The playbook implements the following tasks:

  - 1st: Install Docker containerization platform of choice for our project. 
  - 2nd: Install Python3 compatible programming language used for our project.
  - 3rd: Install the Docker Python module, Installs remaining modules needed to allow docker to work efficiently using Python.


The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
