# Minimal RSP and RSC Installations on VirtualBox VMs

This directory contains everything you need to run two virtual machines, one for RStudio Server Pro and one for RStudio Connect. Virtualization is provided on VirtualBox, the machines are managed through Vagrant, and provisioning is handled with Ansible.

### First

- [Install VirtualBox](https://www.virtualbox.org/)
- [Install Vagrant](https://www.vagrantup.com/downloads.html)
- [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-control-machine): `pip install ansible`

### Download Ubuntu 16.04 Box

Retrieve a pre-built [Ubuntu image from Vagrant Cloud](https://app.vagrantup.com/bento/boxes/ubuntu-16.04):

```
vagrant box add bento/ubuntu-16.04
```

### Run

From this directory:

- To boot all machines: `vagrant up`
- To make a change: `vagrant provision`
- To stop all machines: `vagrant halt`
- To tear down all machines: `vagrant destroy` (confirmation req. for each)

Optional:
- Boot up just the RStudio Server Pro machine: `vagrant up rsp`
- Boot up just the RStudio Connect machine: `vagrant up rsc`
- Boot up just the RStudio Package Manager machine: `vagrant up rspm`


### Access

- To SSH into RStudio Server Pro: `vagrant ssh rsp`
- To SSH into RStudio Connect: `vagrant ssh rsc`
- To SSH into RStudio Package Manager: `vagrant ssh rspm`

The machines need to networked together, or else you wont be able to serve packages from RSPM or push-button publish from RSP to RSC. These addresses can be changed/adjusted as needed in the Vagrantfile.

To that end, the services will be available at the following IP addresses:

 - RStudio Server Pro IDE: `10.0.0.10:8787`

    -user: `rstudio`
    -password: `rstudio`

 - RStudio Connect: `10.0.0.11:3939`

    -sign-in to create a demo admin account

 - RStudio Package Manager `10.0.0.12:4242`

 	- user: `rstudio`
 	- password: `rstudio`
