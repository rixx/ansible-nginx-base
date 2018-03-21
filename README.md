rixx.nginx-base
===============

A role to install nginx, including sensibly secure configuration according to latest Mozilla guidelines, and an UFW
rule. Works with Debian, Ubuntu, and Arch Linux.


Role Variables
--------------

``mozilla_configuration: modern|intermediate|old`` (default: ``modern``)

This is one of the three possible Mozilla recommendated SSL configuration levels, as can be seen here (including
compatible systems): https://statics.tls.security.mozilla.org/server-side-tls-conf.json



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: rixx.ansible-base, x: 42 }

License
-------

BSD

Author Information
------------------

rixx <r at rixx.de>
