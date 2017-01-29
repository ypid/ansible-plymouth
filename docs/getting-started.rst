Getting started
===============

.. include:: includes/all.rst

.. contents::
   :local:


Example inventory
-----------------

To configure Plymouth on a host it should be included in the
``ypid_service_plymouth`` Ansible inventory group:

.. code:: ini

   [ypid_service_plymouth]
   hostname

Example playbook
----------------

Here's an example playbook that uses the ``ypid.plymouth`` role:

.. literalinclude:: playbooks/plymouth.yml
   :language: yaml

This playbooks is shipped with this role under :file:`./docs/playbooks/plymouth.yml`
from which you can symlink it to your playbook directory.
In case you use multiple roles maintained by ypid_, consider
using `ypid-ansible-common`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after a host was first
configured to speed up playbook execution, when you are sure that most of the
configuration is already in the desired state.

Available role tags:

``role::plymouth``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::plymouth:pkgs``
  Tasks related to system package management like installing or
  removing packages.
