# ypid-ansible-common

This git repository is tying together ypid’s Ansible building blocks using git submodules.

As every good sysadmin should know what he/she is doing and CM is an essential
tool for every good sysadmin ypid has committed himself to review every CM component
and all changes to those components before running them in production. ypid does
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
of git repositories which ypid has verified and tested.

All commits of this repository are signed with ypid’s OpenPGP automatic signing
key and thus implicitly signs all content and the git history (also applies to
git submodules).

The weakest link of the signature is currently
[SHA-1](https://en.wikipedia.org/wiki/SHA-1) used in by git.
This will be mitigated in the near future by only relying on
strong cryptography (ref:
[Cryptographically strong code signing](https://github.com/QubesOS/qubes-issues/issues/2240)).

ypid uses a [shell script called "update_submodules"](https://github.com/ypid/ypid-ansible-common/blob/master/update_submodules) to pull the latest changes from git remotes, watch over the diffs and then update the master branch of the repository if everything looks good.

## Refs

* https://wiki.debops.org/wiki:user:ypid
