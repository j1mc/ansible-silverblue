shell
=======

Install (but don't really configure) oh-my-zsh.

Requirements
------------

None

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
         - { role: shell }

To Run It
---------

`ansible-playbook -i hosts -l this_host --ask-become-pass roles/shell/playbook.yml`

License
-------

Apache 2

Author Information
------------------

Jim Campbell (jwcampbell@gmail.com)

