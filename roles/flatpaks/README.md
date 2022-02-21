flatpaks
========

Installs requested flatpak software on the host. By default, it will only install and configure
the [flathub](https://flathub.org/home) repository. Other flatpak remotes are available, though!
See the `group_vars/all` file and uncomment the repositories that you want to use.

Requirements
------------

This role assumes that the `flatpak` application is already installed.

Uses the following modules:

  * [ansible.builtin.command](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/command_module.html)
  * [ansible.community.flatpak_remote](https://docs.ansible.com/ansible/latest/collections/community/general/flatpak_remote_module.html)
  * [ansible.community.flatpak](https://docs.ansible.com/ansible/latest/collections/community/general/flatpak_module.html)

Role Variables
--------------

These varables are set in the project's `group_vars/all` file. Make your edits there!

  * flatpak_remote_install: Configure a flatpak remote. Requires a name and a URL.
  * flatpak_package_install: Flatpak applications to install. Requires a `remote` (e.g.,
    'flathub'), and an application name (e.g., 'org.gnome.Podcasts').

Dependencies
------------

None

Example Adhoc Run
-----------------

`ansible-playbook -i hosts -l this_host -K roles/flatpaks/playbook.yml`

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: flatpaks }

License
-------

BSD

Author Information
------------------

  * Jim Campbell (jwcampbell@gmail.com)
