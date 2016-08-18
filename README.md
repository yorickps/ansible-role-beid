beid
=========

Role to install Belgian eiD software

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
