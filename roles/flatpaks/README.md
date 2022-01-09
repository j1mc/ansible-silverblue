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

None

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
