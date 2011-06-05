# Overbox-Base-Repo
This git repository is a YUM repository that contains RPM Packages, needed to
install a CentOS [Vagrant](http://vagrantup.com/) base box via kickstart.

## Usage
Simply install the vagrant-boxification RPM

### Install with kickstart
Add this repo:
```bash
repo --name=overbox-base-repo --baseurl=http://ancientlegrey.github.com/overbox-base-repo/noarch
```

Add vagrant-boxification in the %packages section.

Have a look at the example kickstart file in the kickstart directory. It
produces a woking vagrant base box with minimal package selection.

### Install later
To boxifiy an existing CentOS installation try this:

```bash
cd /etc/yum.repos.d
wget http://ancientlegrey.github.com/overbox-base-repo/overbox-base.repo
yum install vagrant-boxification
```

## Caution
Don't install vagrant-boxification on production servers! It creates the default
user "vagrant" and makes him non-password-sudoer! The installation cannot be
undone with "yum remove".

## Contents
To browse the contents visit the [repoview](http://ancientlegrey.github.com/overbox-base-repo/noarch/repoview/)

## Bugs
Please report bugs with the GitHub issue tracker.
