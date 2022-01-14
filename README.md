ansible-silverblue
==================

You can use this repository to configure a [Fedora Silverblue](https://silverblue.fedoraproject.org/)
workstation or laptop with Ansible.

Each of the project's roles contain a README file that explains what the role is and how to use
it.

Variables
---------

I've tried to consolidate variables into the `group_vars/all` file. Please look at that file!
Edits to that file will affect what happens in each of the related roles.

Included Roles
--------------

  - layered_packages: Install layered packages into the rpm-ostree image.
  - flatpaks: Install desired flatpak packages
  - fonts: Installs custom fonts (this role is under the GPLv3 License)
  - settings: Sets desired GUI settings via dconf.

Setup
-----

Clone this repository with:

  - `git clone https://github.com/j1mc/ansible-silverblue.git`

Install needed dependencies with:

  - `cd ansible-silverblue && python3 -m venv venv`
  - `source venv/bin/activate`
  - `&& pip3 install -r requirements.txt`
  - `ansible-galaxy collection install -r requirements.yml`

Makes edits to the `group_vars/all` file to customize this project to make it do what you want it
to do.

Run the Playbooks
-----------------

This command will run all of the included playbooks:

`ansible-playbook -i hosts -l this_host -K playbook_base.yml`.

License
-------

Unless otherwise indicated in the individual role, this project is under the BSD License.

Author
------

  * Jim Campbell (jwcampbell@gmail.com)
