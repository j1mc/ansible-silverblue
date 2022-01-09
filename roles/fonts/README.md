fonts
=====

Install custom fonts to `~/.local/share/fonts`.

Requirements
------------

This role requires the `fontconfig` package to be installed. That package will be installed in the
`layered_packages` role.

Modules used:

  * community.general.rpm_ostree_pkg
  * ansible.builtin.git
  * ansible.builtin.file
  * ansible.builtin.command

Role Variables
--------------

These variables are tracked in this role's `vars/main.yml` file.

```yaml
all_users:              # this role can configure for one or more users
  - user: foo           # username
    homedir: /home/foo  # the home dir for the username

all_fonts:              # the fonts you want to install
  - RobotoMono          # the name of these fonts must match the name of the
  - SourceCodePro       # font directory
  - DejaVuSansMono
  - UbuntuMono
```

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
