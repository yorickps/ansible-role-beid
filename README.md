ansible-role-beid
=========

[![Build Status](https://travis-ci.org/yorickps/ansible-role-beid.svg?branch=master)](https://travis-ci.org/yorickps/ansible-role-beid)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-beid-blue.svg?style=flat)](https://galaxy.ansible.com/yorickps/beid)

Role to install [Belgian eiD software and middleware](https://eid.belgium.be/en/how-install-eid-software) on Debian and RedHat based systems.

It installs the "eid-archive" package, enabling the eID package repositories. Based on the packages enabled in the vars, the role installs the "eid-viewer" and/or "eid-mw" packages.

This role does ***not*** cover the installation of the smart card reader. More info can be found on the
[eiD FAQ](http://test.eid.belgium.be/faq/faq_nl.htm) from the Belgian governement and the [Debian Smartcards wiki](https://wiki.debian.org/Smartcards).

For Firefox, an [add-on](https://addons.mozilla.org/en-US/firefox/addon/belgium-eid/) is required.

Requirements
------------

Role must be run with elevated rights (become sudo or root)

Role Variables
--------------


```
eid_latest_version: check OS specific vars
```

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles:
         - { role: yorickps.beid }


License
-------

BSD

Author Information
------------------

yorickps
