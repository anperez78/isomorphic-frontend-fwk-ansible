# Ansible Vagrant profile for Isomorphic Frontend Framework (demo)

## Background

Vagrant and VirtualBox (or some other VM provider) can be used to quickly build or rebuild virtual servers.

This Vagrant profile installs the [Isomorphic framework web project](https://github.com/anperez78/isomorphic-frontend-framework) using the [Ansible](http://www.ansible.com/) provisioner.

## Getting Started

This README file is inside a folder that contains a `Vagrantfile` (hereafter this folder shall be called the [vagrant_root]), which tells Vagrant how to set up your virtual machine in VirtualBox.

To use the vagrant file, you will need to have done the following:

  1. Download and Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
  2. Download and Install [Vagrant](https://www.vagrantup.com/downloads.html)
  3. Install [Ansible](http://ansibleworks.com/) ([guide for installing Ansible](http://docs.ansible.com/intro_installation.html))
  4. Open a shell prompt (Terminal app on a Mac) and cd into the folder containing the `Vagrantfile`

Once all of that is done, you can simply type in `vagrant up`, and Vagrant will create a new VM, install the base box, and configure it.

Once the new VM is up and running (after `vagrant up` is complete and you're back at the command prompt), you can log into it via SSH if you'd like by typing in `vagrant ssh`. Otherwise, the next steps are below.

### Setting up your hosts file

You need to modify your host machine's hosts file (Mac/Linux: `/etc/hosts`; Windows: `%systemroot%\system32\drivers\etc\hosts`), adding the line below:

    192.168.100.30 isomorphic.local

(Where `nodejs`) is the hostname you have configured in the `Vagrantfile`).

After that is configured, you could visit [http://isomorphic.local:3000](http://isomorphic.local:3000) in a browser, and you'll see the first page from the React demo application.

# License

This projected is licensed under the terms of the MIT license.
