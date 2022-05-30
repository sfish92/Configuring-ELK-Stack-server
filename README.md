# Cyber-Bootcamp-Project-1
Week 13 Project Submission

## Automated ELK Stack Development

The files in this repository were used to configure the network depicted below.

[Cloud Security Network Diagram ](https://user-images.githubusercontent.com/81527445/170909141-e8cca7e8-27e2-446f-bcb2-bf32a0b84152.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YAML and Config files may be used to install only certain pieces of it, such as filebeat.

TO enter playbook file

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in use
  - Machines being monitored
- How to use the Ansible Build

### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D#mn Vulnerable Web Application.

Load balancing ensures that the application will be highly functional, in addition to restricting traffic to the network.
- What aspect of security do load balancers protect? 
  - Without a load balancer your network is more susceptible to be attacked via a DoS (Denial of     Service).  

  - What is the advantage of a jump box?

Integrating an ELK server allows users to easily monitor the vulnerable VMs for the changes to the _______ and system ______.
- What does Filebeat watch for?
- What does Metricbeat record?

The configuration details of each machine may be found below.

| Name     | Function      | IP Address    | Operating System |
|----------|---------------|---------------|------------------|
| Jump Box | Gateway       | My Local IP   | Linux            |
| Web-1    | Ubuntu Server | 10.0.0.5      | Linux            |
| Web-2    | Ubuntu Server | 10.0.0.6      | Linux            |
| Elk-VM   | Elk Server    | 10.1.0.4      | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet.

Only the Jump Box Provisioner can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- My Local IP Address via an SSH connection.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | No                  | My Local IP          |
| Web-1    | No                  | 10.0.0.4             |
| Web-2    | No                  | 10.0.0.4             |
| Elk-VM   | No                  | 10.0.0/6             |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- What is the main advantage of automating configuration with Ansible?
  - Trying to set up an environment without Ansible would be very difficult and time consuming.     The best part about ansible is it's flexibility: allowing you to manage the entire               environment no matter the location. No major coding skills are required to create Ansible's     playbooks making it simple to set up and utilize.

The playbook implements the following tasks:

The following screenshot displays the result of running 'docker ps' after sucessfully configuring the ELK instance.

TODO Image with docker ps

### Target Machine & Beats
This ELK server is configured to monitor the following machines:
- 10.0.0.5
- 10.0.0.6

We have installed the following Beats on these machines:
- TODO ADD SCREENSHOT of beats sucessfully installed

These Beats allow us to collect the following information from each machine:
- TODO

### Using the Playbook

In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:
- Copy the YAML file to the ansible directory.
- Update the config file to include the internal IP along with specified ports. 
- In order to check that the ELK server is running navigate to:                                   http://[ELK.VM.IP]:5601/app/kibana

