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

&nbsp;
&nbsp;

This vagrant machine uses an NFS folder to allow us to edit code in our local environment.  You will see the following message asking for admin permissions to configure this on first run.  Please enter your local user admin password when prompted.

> ==> systemsup: Exporting NFS shared folders...
> ==> systemsup: Preparing to edit /etc/exports. Administrator privileges will be required...

> WARNING: Improper use of the sudo command could lead to data loss
> or the deletion of important system files. Please double-check your
> typing when using sudo. Type "man sudo" for more information.

> To proceed, enter your password, or type Ctrl-C to abort.

> Password:

&nbsp;
&nbsp;
&nbsp;

Due to an issue with Puppet provisioning on the first run, some python packages will fail to install and the following error message will be displayed after the first 'vagrant up' is run:

> The SSH command responded with a non-zero exit status. Vagrant
> assumes that this means the command failed. The output for this command
> should be in the log above. Please read the output to determine what
> went wrong.

To ensure the packages are installed correctly, re-run 'vagrant provision' immediately.

```sh
$ vagrant provision
```
