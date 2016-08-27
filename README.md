beid
=========

[![Build Status](https://travis-ci.org/ymajik/ansible-role-beid.svg?branch=master)](https://travis-ci.org/ymajik/ansible-role-beid)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-beid-blue.svg?style=flat)](https://galaxy.ansible.com/ymajik/beid)

Role to install [Belgian eiD software and middleware](http://eid.belgium.be/en/using_your_eid/installing_the_eid_software/linux) on Debian based systems.

It installs the "eid-archive" package, enabling the eID package repositories. Based on the packages enabled in the vars, the role installs the "eid-viewer" and/or "eid-mw" packages.

This role does ***not*** cover the installation of the smart card reader. More info can be found on the
[eiD FAQ](http://test.eid.belgium.be/faq/faq_nl.htm) from the Belgian governement and the [Debian Smartcards wiki](https://wiki.debian.org/Smartcards).

For Firefox, an [add-on](https://addons.mozilla.org/en-US/firefox/addon/belgium-eid/) is required.

Requirements
------------

None

Role Variables
--------------


```
eid_browser_packages:
  - icedtea-plugin
  - default-jre
eid_packages:
  - eid-archive
  - eid-viewer
  - eid-mw
eid_version: 2016.3
eid_url: http://eid.belgium.be/sites/default/files/downloads/eid-archive_{{ eid_version }}_all.deb
```

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles:
         - { role: ymajik.ansible-role-beid }
      vars:
        eid_version: 2016.3

License
-------

BSD

Author Information
------------------

ymajik
