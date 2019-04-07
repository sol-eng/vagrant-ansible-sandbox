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

- R Package Installation: `shiny`, `tidyverse`, `rmarkdown` installed by default, change to option and default to RSPM for packages.
- Add scripts for HA
- Document options and recs for increased memory on the VM(s) 
- Modular-ize Ansible playbooks (worth it?)
- Add floating license server setup
