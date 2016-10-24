Role Name
=========

An Ansible role that installs the lastest version of libmraa

Requirements
------------

If programming in Python, the correct version of Python must be installed on the target.

Role Variables
--------------

Available variables are listed below, along with default values:

    mraa_ppa: "ppa:mraa/mraa"

(Optionally enable programming in Python)

    mraa_wrappers:
      python:
        lib_name: "python-mraa"
        install: no
      python3:
        lib_name: "python3-mraa"
        install: no

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: plengoer.mraa
          become: yes
      vars:
        mraa_wrappers:
          python:
            lib_name: "python-mraa"
            install: yes
          python3:
            lib_name: "python3-mraa"
            install: yes

License
-------

MIT

Author Information
------------------

This role was created in 2016 by James Giller, PLENGoer Robotics Inc.
