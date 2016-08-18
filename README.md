Role Name
=========

Role to install Belgian eiD software

Requirements
------------

None

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

```
eid_browser_packages:
  - icedtea-plugin
  - default-jre
eid_packages:
  - eid-archive
  - eid-viewer
  - eid-mw
eid_version: 2016.2
eid_url: http://eid.belgium.be/sites/default/files/downloads/eid-archive_{{ eid_version }}_all.deb
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - { role: ymajik.ansible-role-beid }
      vars:
        eid_version: 2016.2

License
-------

BSD

Author Information
------------------

ymajik
