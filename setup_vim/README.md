setup_vim
=========

My everyday Vim setup, so not really useful for anyone but me. Tested with
Molecule on Debian 10/11, but should work on any modern Debian-based OS.

Role Variables
--------------

The list of Vim plugins to be installed is in defaults/main.yml. Edit as
needed.

Example Playbook
----------------

    - name: Configure Vim
      hosts: all
      gather_facts: yes
      become: no
      roles:
         - setup_vim

`ansible-playbook -i <ip-address or localhost>, -b -k -K`

Sometimes we don't want the extra plugins (CoC and ansible stuff) installed,
so we'll run the playbook with `--skip-tags "extra"`. Also, if we have vim and
git already installed, we can skip the package installation task with
`--skip-tags "install_packages"`

License
-------

MIT

Author Information
------------------

[tyybbi](https://github.com/tyybbi)
