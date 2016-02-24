Role Name
=========

This role removes the .disabled extension that hosting companys sometimes adds to default cronjobs to disable them and save cpu cycles. These cronjobs generally exist for a cause and should be run if there is no reason against it.

Requirements
------------

No requirements.

Role Variables
--------------

* `cronjob_enable_blacklist`: list of cronjobs that should not get enabled

Example Playbook
----------------

    - hosts: servers
      roles:
         - enable-standard-cronjobs

    - hosts: servers
      roles:
         - { role: enable-standard-cronjobs, cronjob_enable_blacklist: ['passwd'] }

License
-------

GPLv2

Author Information
------------------

Yannik Sembritzki
