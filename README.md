ansible-aosp
============

This Ansible role sets up an AOSP build environment. The role can be used as follows

    - hosts: localhost
      roles:
         - role: fegge.ansible-aosp
           source_tag: android-7.1.1_r1

When the host is provisioned, you need to download the precompiled drivers (e.g. from https://developers.google.com/android/drivers) and run the self-extracting script in the root of the source tree. 

To build the source, you run

    . build/envsetup.sh
    lunch <menu item>
    make -j4


Role Variables
--------------

To use this role, you need to define the variable `source_tag`. It is also possible to specify `source_dir`, and `build_dir`.


Example Playbook
----------------

The role can be used as follows

    - hosts: localhost
      roles:
         - role: fegge.aosp
           source_tag: android-7.1.1_r1


License
-------

GPLv2

