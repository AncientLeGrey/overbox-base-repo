# Overbox-Base-Repo
This git repository is a YUM repository that contains RPM Packages, needed to
install a CentOS [Vagrant](http://vagrantup.com/) base box via kickstart.

## Usage
Simply install the vagrant-boxification RPM.

### Install with kickstart
Add these two yum-repos in your ks file:

* repo --name=overbox-base-repo --baseurl=http://ancientlegrey.github.com/overbox-base-repo/noarch
  repo --name=rpmforge --baseurl=http://apt.sw.be/redhat/el5/en/i386/rpmforge

* List vagrant-boxification in the %packages section.

Have a look at the example kickstart file in the kickstart directory. It
produces a woking vagrant base box with minimal package selection.

### Or install later with yum
To boxifiy an existing CentOS installation try this:

```bash
cd /etc/yum.repos.d
wget http://ancientlegrey.github.com/overbox-base-repo/overbox-base.repo
yum install rpmforge-release
yum install vagrant-boxification
```

## Caution
Don't install vagrant-boxification on production servers! It creates the unsafe default
user "vagrant" and makes him non-password-sudoer! The installation cannot be
undone with "yum remove".

## Contents
To browse the contents visit the [repoview](http://ancientlegrey.github.com/overbox-base-repo/noarch/repoview/)

## Bugs
Please report bugs with the GitHub issue tracker.
