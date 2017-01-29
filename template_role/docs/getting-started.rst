Getting started
===============

.. include:: includes/all.rst

.. contents::
   :local:


Example inventory
-----------------

To manage `changeme/FIXME**, on a host it should be included in the
``debops_service_ROLE_NAME`` Ansible inventory group:

.. code:: ini

   [debops_service_ROLE_NAME]
   hostname

Example playbook
----------------

If you are using this role without DebOps, here's an example Ansible playbook
that uses the ``ROLE_OWNER.ROLE_NAME`` role:

.. literalinclude:: playbooks/ROLE_NAME.yml
   :language: yaml

The playbooks is shipped with this role under
:file:`./docs/playbooks/ROLE_NAME.yml` from which you can symlink it to your
playbook directory.
In case you use multiple `DebOps Contrib`_ roles, consider
using the `DebOps Contrib playbooks`_.
`changeme/FIXME**
In case you use multiple `DebOps Contrib`_ roles, consider using the
`DebOps Contrib playbooks`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::ROLE_NAME``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::ROLE_NAME:pkgs``
  Tasks related to system package management like installing or
  removing packages.
