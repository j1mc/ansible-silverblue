os_updates
==========

Configure operating system updates for Fedora Silverblue hosts.

Requirements
------------

Modules used:

  * [ansible.builtin.template](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/template_module.html)

Role Variables
--------------

  * `update_policy`: "none", "check", or "stage".
    * none: (default) disables automatic updates.
    * check: Downloads just enough metadata to check for updates and display the updates in
      rpm-ostree status.
    * stage: Downloads and unpacks the update, performing any package layering. The updates are
      applied after a reboot.
  * `idle_timeout`: Controls the time in seconds of inactivity before the rpm-ostree daemon exits.
    * 60 seconds (default)
    * Set to `0` to disable the idle timeout.

Dependencies
------------

None

Example Adhoc Run
-----------------

`ansible-playbook -i hosts -l this_host -K roles/os_updates/playbook.yml`

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: os_updates}

License
-------

BSD

Author Information
------------------

  * Jim Campbell (jwcampbell@gmail.com)
