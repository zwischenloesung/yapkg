YAPKG
=====

This is Yet-Another-PacKaGe-installer role for ansible.

Why we do not use one of the existing?

* For the first reason read the section "Promise" below. We need something reliable.
* This role will be used by [maestro](https://github.com/inofix/maestro) and must follow the logic used there. (Of course, the role can be used without maestro..)

Promise
-------

Sure this role may change in the future, but we will only expand features to not break backwards compatibility.

If radical changes should become necessary, a new role will be created, probably with an 'ng' or version suffix...


Installation
------------

 # ansible-galaxy install zwischenloesung.yapkg

Requirements
------------

* Ansible >2.0

Role Variables
--------------

* yapkg\_names

Dependencies
------------

* Currently only "Debian" is supported
* It will test for the OS/Distro, namely
 * 'ansible\_os\_family'

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: zwischenloesung.yapkg, yapkg_names: [ foo, bar ] }

License
-------

GPLv3

Author Information
------------------

* Michael Lustenberger at [inofix.ch](http://www.inofix.ch)
