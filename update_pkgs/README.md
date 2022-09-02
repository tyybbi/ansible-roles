update_pkgs
=========

Simple role to update packages to their latest version and run some cleanup
tasks afterwards.

Role Variables
--------------

Edit APT options as needed in defaults/main.yml.

Requirements
------------

A Debian-based OS.

Example Playbook
----------------

    - name: Update OS
      hosts: all
      gather_facts: yes
      become: yes
      roles:
         - update_pkgs

- Locally: `ansible-playbook -i localhost, --connection=local -K`
- Remotely: `ansible-playbook -i <IP address>, -k -K`
License
-------

MIT

Author Information
------------------

[tyybbi](https://github.com/tyybbi)
