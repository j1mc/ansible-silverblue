Settings
========

Use `dconf` to apply desired user interface settings. Currently, this role sets the following
options:

  - Enables the 'Night Light' feature.


Requirements
------------

Requires `python3-psutil`. This package is installed as a 'layered' package in the
`layered_packages` role.

Role Variables
--------------

Prescribed dconf settings are set in `vars/main.yml`.  You can identify other settings you may
want to use by entering `dconf watch /` in a terminal, and then making your desired changes. As
you make changes, the dconf updates will be reflected in the terminal output.

Dependencies
------------

None

Example Adhoc Run
-----------------

`ansible-playbook -i hosts -l this_host -K roles/settings/playbook.yml`

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: settings }

License
-------

BSD

Author Information
------------------

  * Jim Campbell (jwcampbell@gmail.com)