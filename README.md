# Intro to Ansible ELAG 2019 - Development Environment
A workshop by Chad Nelson / [bibliotechy](https://github.com/bibliotechy) / [@bibliotechy](https://twitter.com/bibliotechy)

## What you'll find here

This repository contains the basic configuration for a Vagrant machine that we will run while building an Ansible playbook together.

### Other branches
Two other branches are also present, which contain end goals for some of the work we will do together during the workshop. Feel free to peak at them if you are interested, but I will be expected you to work through the exercise I have put together, during the workshop.

## What you need to get started

You will need a few things installed before you can get started. Follow the instructions for you OS.

* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](http://docs.ansible.com/ansible/intro_installation.html#installation) - latest release is fine.

Once you have the above prerequisites installed, you'll need to clone this github repository and import the base vagrant box that we'll be buidling on. Doing in this advance of the workshop will ensure that we don't overwhelm the conference wifi.
```
$ git clone https://github.com/bibliotechy/elag-2019-ansible-workshop.git
$ cd elag-2019-ansible-workshop
$ vagrant up
> Bringing machine 'default' up with 'virtualbox' provider...
> ...
==> default: Rsyncing folder: /Users/cbn/projects/elag-ansible-vagrant/ => /vagrant

```

At this point it will run through an initial build. Once complete, yuo are done and ready for the workshop You can now shut down your virtual machine and it'll be ready to go for the workshop. You shut it down with:

```
vagrant halt
```
