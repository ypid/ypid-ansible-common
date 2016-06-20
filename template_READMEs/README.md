# Ansible role READMEs

READMEs for repositories of Ansible role in the DebOps project and for my
personal roles are generated using [Ansigenome][].

This directory contains the templates and the verified version of Ansigenome
that I am using.

As I maintain both roles in the DebOps Project and my personal roles, I need to
be able to generate READMEs with different defaults and templates. For this I
use a [wrapper script](../bin/ansigenome-gen) around Ansigenome which enables the correct configuration for
Ansigenome based on the role owner and then runs Ansigenome to (re)generate the
README.md.

[Ansigenome]: https://github.com/nickjj/ansigenome
