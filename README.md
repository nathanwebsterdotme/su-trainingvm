# README

## Pre-Requisites
Please ensure the following versions of applications are installed on your machine prior to going any further.
- Virtualbox v5.016 or above (https://www.virtualbox.org/)
- Vagrant v1.8.1 (https://www.vagrantup.com/)

After Vagrant is installed, run the following command to install a required vagrant plugin:
```sh
$ vagrant plugin install vagrant-bindfs
```

## Instructions
Follow these steps to run the vagrant machine.

Clone the repository to your home directory 

```sh
$ cd ~
$ git clone https://github.com/nathanwebsterdotme/su-trainingvm.git
```

Bring the Vagrant box up:

```sh
$ cd su-trainingvm
$ vagrant up
```

Due to an issue with Puphpet provisioning, some python packages will fail to install when the first 'vagrant up' is run.  You will likely see an error message similar to the following: 

> The SSH command responded with a non-zero exit status. Vagrant
> assumes that this means the command failed. The output for this command
> should be in the log above. Please read the output to determine what
> went wrong.

The recommended work around is to re-run vagrant provision immediately.

```sh
$ vagrant provision
```
