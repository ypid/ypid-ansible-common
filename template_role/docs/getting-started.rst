Getting started
===============

.. contents::
   :local:

.. include:: includes/all.rst


Example inventory
-----------------

To setup and manage the X2go server, add the hosts to the
``debops_service_cryptsetup`` Ansible inventory host group:

.. code:: ini

   [debops_service_cryptsetup]
   hostname

Example playbook
----------------

Here's an example playbook that can be used to setup and manage X2go server:

.. literalinclude:: playbooks/cryptsetup.yml
   :language: yaml

This playbooks is shipped with this role under
:file:`docs/playbooks/cryptsetup.yml` from which you can symlink it to your
playbook directory.
In case you use multiple `DebOps Contrib`_ roles, consider
using the `DebOps Contrib playbooks`_.
`changeme/FIXME**
In case you use multiple roles maintained by ypid_, consider
using the `ypid-ansible-common`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::cryptsetup``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::cryptsetup:backup``
  Tasks related to LUKS header backup.
