ansible-role-hp-diag
=========

Sets up a cronjob that fetches hpssacli diag reports and makes them readable by the nrpe user. Installs python-hpadureport-parser.py that a nagios script can use to parse the diag reports.

Requirements
------------

An HP server that has "hpssacli" installed

 - https://github.com/martbhell/python-hpadureport
  - the python script that returns disks with increasing error values
 - https://github.com/CSC-IT-Center-for-Science/ansible-role-nrpe
  - sets up sudo for nrpe
 - https://github.com/CSC-IT-Center-for-Science/ansible-role-nrpe-plugins
  - copies in the nagios check
 - https://github.com/CSC-IT-Center-for-Science/ansible-role-hp-spp
  - installs the HPe tools

Role Variables
--------------

see defaults/main.yml


Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-hp-spp }
         - { role: ansible-role-hp-diag }

License
-------

MIT

Author Information
------------------
