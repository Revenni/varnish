revenni.varnish
=========

Ansible role providing standalone varnish deployment

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)
[![Licence](https://img.shields.io/badge/Licence-MIT-blue.svg)](https://tldrlegal.com/license/mit-license)

Requirements
------------

* None

Role Variables
--------------

### Generic variables (declared in defaults/main.yml + overridden in vars/main.yml)
* ```varnish_port``` (80) - port varnish should bind to
* ```varnish_mgmt_port``` (6082) - port varnish mgmt should bind to
* ```varnish_mgmt_addr``` (localhost) - bind address for varnish mgmt
* ```varnish_cache_size``` (2g) - size of cache
* ```varnish_vcl_file``` (/etc/varnish/default.vcl) - path to varnish vcl
* ```varnish_secret_file``` (/etc/varnish/secret) - path to varnish secret
* ```varnish_secret``` (bigsecret) - secret for varnish

Dependencies
------------

* None

Example Playbook
----------------

    - hosts: caches
      become: true
      roles:
         - { role: revenni.varnish, tags: varnish }

License
-------

MIT

Author Information
------------------
* [Vince Hillier](https://revenni.com) | [@email](mailto:vince@revenni.com) | [twitter](https://twitter.com/vincedotca)
