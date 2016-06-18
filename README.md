# ypid-ansible-common

This git repository is tying together my Ansible building blocks using git submodules.

As every good sysadmin should know what he/she is doing and CM is an essential
tool for every good sysadmin I committed myself to review every CM component
and all changes to those components before running them in production. I do
this for the following reasons:

* To catch unintentionally/internally introduced flaws
* To ensure that the component does what it says

## How it works

This repository mainly consists of git submodules point to the last version of
an git repository which I have verified and tested.

All commits of this repository are signed with my PGP automatic signing key
which includes/signs all contents of the particular version and the git history
of all submodules.

## Refs

* https://wiki.debops.org/wiki:user:ypid
