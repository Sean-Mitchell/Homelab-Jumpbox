# Homelab Jumpbox

## Goals
The goal of this repository is to create and provision a jumpbox VM via Vagrant and Ansible for downstream deployments to my homelab.
That way the host doesn't get cluttered wtih tests

## Vagrant setup
1. [Download](https://developer.hashicorp.com/vagrant/downloads)
1. Open cmd in the /Vagrant folder
1. Run `vagrant init bento/ubuntu-24.04`
1. Modify the output Vagrantfile to have 
    - 8GB of RAM
    - 6 CPU cores
    - 40GB Primary disk
    - inits with a GUI
    - custom name of `Homelab-test`
1. Run `vagrant up` from the `/Vagrant/` folder
    - Provisioner will get auto downloaded
    - The `/Vagrant/` folder should get mounted as the default shared drive
1. When done run `vagrant destroy -f` to destroy the VM

# Acknowledgements
## Jeff Geerling
Snippets taken from [ansible-for-devops](https://github.com/geerlingguy/ansible-for-devops/) repo and youtube series.

## Jim's Garage
Secrets management and command examples taken from [this video](https://youtu.be/DoiBm5VC-oo)

## GenAI cause it's a great rubber ducky