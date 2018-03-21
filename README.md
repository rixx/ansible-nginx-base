rixx.nginx-base
===============

A role to install nginx, including sensibly secure configuration according to latest Mozilla guidelines, and an UFW
rule. Works with Debian, Ubuntu, and Arch Linux.


Role Variables
--------------

- ``mozilla_configuration: modern|intermediate|old`` (default: ``modern``). This is one of the three possible Mozilla recommendated SSL configuration levels, as can be seen here (including
compatible systems): https://statics.tls.security.mozilla.org/server-side-tls-conf.json
- ``nginx_user: http``
- ``nginx_dhparams_path: /etc/ssl/nginx.dhparams``
- ``nginx_hsts: false``: Set to ``true`` to enable HSTS.
- ``nginx_hsts_age: 15768000``: Set HSTS protection age in seconds.
- ``nginx_sites_path: /etc/nginx/sites``
- ``nginx_worker_processes: false``: Set to ``true`` to enable auto worker processes.
- ``nginx_global_custom``: A string to be included on the uppermost config level, next to the ``http`` directive.
- ``nginx_acme_challenge: true``: Provide an acme challenge configuration.
- ``nginx_acme_challenge_path: /usr/share/nginx/letsencrypt``: Poing acme challenges here.
- ``nginx_ufw_path: /etc/ufw/applications.d``: The ufw application config path


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
