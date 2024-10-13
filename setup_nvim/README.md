setup_nvim
=========

Build Neovim from source, create and install the .deb package with my preferred
configuration and plugins. Tested with Molecule on Debian 12, but should work
on any modern Debian-based distro. Not idempotent, but does its job.

Note that possible LSP dependencies (such as Go) are not installed in this role.

Role Variables
--------------

A description of the settable variables for this role should go here, including
any variables that are in defaults/main.yml, vars/main.yml, and any variables
that can/should be set via parameters to the role. Any variables that are read
from other roles and/or the global scope (ie. hostvars, group vars, etc.) should
be mentioned here as well.

Example Playbook
----------------

    - name: Configure Neovim
      hosts: all
      gather_facts: yes
      become: no
      roles:
         - setup_nvim

- Locally: `ansible-playbook -i 127.0.0.1, -c local -K`
- Remotely: `ansible-playbook -i <IP address>, -kK -u <usernam>`

License
-------

MIT

Author Information
------------------

[tyybbi](https://github.com/tyybbi)
