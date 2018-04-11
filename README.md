# Cumulus-OSPF-Lab
This lab is intended to give the user a enviroment where two Cumulus VX routers have a ospf adj across a vEOS switch. Each Cumulus router has a server attached to it for end to end testing.

![arch](/docs/imgs/Cumulus-OSPF-Lab_topology.jpg "Lab Topology")

## Setup

### Required Software
Download and install: 
 - VirtualBox
 - Vagrant

#### Vagrant
This will require the following vagrant boxes be available on your system:
- CumulusCommunity/cumulus-vx version 3.1.2
- olbat/tiny-core-micro version 0.1.0
- vEOS-lab-4.17.3F version 0 (https://eos.arista.com/using-veos-with-vagrant-and-virtualbox/)

#### VirtualBox
Provider/hypervisor to run the vagrant controlled VM's.