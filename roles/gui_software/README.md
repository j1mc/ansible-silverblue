gui_software
============

Installs requested software on the host.

Requirements
------------

Uses the following modules:

  * `package`,
  * `flatpak_remote`
  * `flatpak`
  * `rpm_key`
  * `yum_repository`

Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: gui_software }

License
-------

BSD

Author Information
------------------

Jim Campbell (jcampbell@gnome.org)

