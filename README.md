# ypid-ansible-common

This git repository is tying together my Ansible building blocks using git submodules.

As every good sysadmin should know what he/she is doing and CM is an essential
tool for every good sysadmin I committed myself to review every CM component
and all changes to those components before running them in production. I do
this for the following reasons:

* To catch unintentionally/internally introduced flaws
* To ensure that the component does what it says

Note that this does not include the CM engine (Ansible).
Ansible core is trusted.
Components in
[ansible-modules-extras](https://github.com/ansible/ansible-modules-extras)
might receive a review when it feels appropriate.

## How it works

This repository mainly consists of git submodules pointing to the last version
of git repositories which I have verified and tested.

All commits of this repository are signed with my OpenPGP automatic signing key
implicitly signs all content and the git history (also applies to git submodules).

I use a [shell script called "update_submodules"](https://github.com/ypid/ypid-ansible-common/blob/master/update_submodules) to pull the latest changes from git remotes, show me the diffs and then update my master branch of the repository if everything looks good.

## Refs

* https://wiki.debops.org/wiki:user:ypid
