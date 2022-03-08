ansible-silverblue
==================

You can use this repository to configure a [Fedora Silverblue](https://silverblue.fedoraproject.org/)
workstation or laptop with Ansible. It will make it easier to apply the same settings to multiple
hosts, saving you from having to manually configure your computer over and over again.

Included Roles
--------------

The main parts of this project can be seen in the 'roles' directory. Each role included there
contains a README file that explains what the role is and how to use it. For starters, here is a
brief summary of each role:

  - layered_packages: Install or remove packages into / from the base rpm-ostree image.
  - flatpaks: Install desired [flatpak](https://flatpak.org/) applications.
  - fonts: Install custom fonts (this role is under the GPLv3 License).
  - gnome_settings: Set various GNOME desktop settings. The role makes these changes via
    [dconf](https://wiki.gnome.org/Projects/dconf).
  - os_updates: Configure the auto-update policy for the host.

Variables
---------

I've consolidated the project's variables into the `group_vars/all` file. This makes it easy to
update the project's variables from a single location. You should customize the values in that
file to set what changes get applied in the various roles.

Setup
-----

Clone this repository with:

  - `git clone https://github.com/j1mc/ansible-silverblue.git`

Install needed dependencies with:

  - `cd ansible-silverblue`
  - `python3 -m venv venv`
  - `source venv/bin/activate`
  - `pip3 install -r requirements.txt`
  - `ansible-galaxy collection install -r requirements.yml`

... then make edits to the `group_vars/all` file to customize this project to make it do what you
want it to do.

Run the Playbooks
-----------------

This command will run all of the included playbooks:

`ansible-playbook -i hosts -l this_host -K -v playbook_base.yml`

If you want to run any of the roles individually, please review that role's `README` file for the
needed command.

License
-------

Unless otherwise indicated in the individual role, this project is under the BSD License.

Author
------

  * Jim Campbell (jwcampbell@gmail.com)
