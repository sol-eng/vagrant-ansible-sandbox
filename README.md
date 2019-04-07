# VM QuickLaunch Playbooks for Vagrant + Ansible + VirtualBox

### First

- [Install VirtualBox](https://www.virtualbox.org/)
- [Install Vagrant](https://www.vagrantup.com/downloads.html)
- [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-control-machine): `pip install ansible`

### Currently Available:

- [CentOS 7](/centos-rsp-rsc)
  - RStudio Server Pro
  - RStudio Connect
  - RStudio Package Manager

- [Ubuntu 16.04](/ubuntu-rsp-rsc)
  - RStudio Server Pro
  - RStudio Connect

### Future Improvements

At the moment, the `shiny`, `tidyverse`, and `rmarkdown` packages are installed on all 3 servers by default. Future releases should probably default to connecting to RSPM for package management.

- Document options and recs for increased memory on the VM(s) 
