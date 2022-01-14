flatpaks
========

Installs requested flatpak software on the host.

Requirements
------------

This role assumes that the `flatpak` application is already installed.

Uses the following modules:

  * `ansible.community.flatpak_remote`
  * `ansible.community.flatpak`

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
