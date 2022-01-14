layered_packages
================

This role installs and removes [layered_packages](https://docs.fedoraproject.org/en-US/iot/add-layered/)
onto an rpm-ostree host such as Fedora Silverblue.

The role will work better after rpm-ostree's `--apply-live` feature is available via
[this pull request](https://github.com/ansible-collections/community.general/pull/3908).

Requirements
------------

Modules used:

  * [community.general.rpm_ostree_pkg](https://docs.ansible.com/ansible/latest/collections/community/general/rpm_ostree_pkg_module.html)
  * [ansible.builtin.command](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/command_module.html)

Role Variables
--------------

These varables are set in the project's `group_vars/all` file. Make your edits there!

  * layered_package_install: Install these packages as layered packages.
  * layered_package_remove: Remove these packages as layered packages.

Dependencies
------------

None

Example Adhoc Run
-----------------

`ansible-playbook -i hosts -l this_host -K roles/layered_packages/playbook.yml`

Example Playbook
----------------

    - hosts: all
      roles:
        - { role: layered_packages }

License
-------

BSD

Author Information
------------------

  * Jim Campbell (jwcampbell@gmail.com)
