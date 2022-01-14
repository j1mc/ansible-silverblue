fonts
=====

Install custom fonts to `~/.local/share/fonts`.

Requirements
------------

This role requires the `fontconfig` package to be installed. That package will be installed in the
`layered_packages` role.

Modules used:

  * [ansible.builtin.command](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/command_module.html)
  * [ansible.builtin.file](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html)
  * [ansible.builtin.git](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/git_module.html)
  * [community.general.rpm_ostree_pkg](https://docs.ansible.com/ansible/latest/collections/community/general/rpm_ostree_pkg_module.html)

Role Variables
--------------

These varables are set in the project's `group_vars/all` file. Make your edits there!

  * all_fonts: Fonts to be installed

Dependencies
------------

None

Example Adhoc Run
-----------------

`ansible-playbook -i hosts -l this_host -K roles/fonts/playbook.yml`

Example Playbook
----------------

    - hosts: all
      roles:
        - { role: fonts }

License
-------

GPLv3

Author Information
------------------

  * Tiago M. Vieira - [https://github.com/tvieira](https://github.com/tvieira)
  * Jim Campbell (jwcampbell@gmail.com)
