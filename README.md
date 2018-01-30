## collectd-plugin-haproxy

[![Build Status](https://travis-ci.org/Oefenweb/ansible-collectd-plugin-haproxy.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-collectd-plugin-haproxy) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-collectd--plugin--haproxy-blue.svg)](https://galaxy.ansible.com/Oefenweb/collectd-plugin-haproxy)

Ansible role to set up the [SignalFx HAProxy plugin](https://github.com/signalfx/collectd-haproxy) for Collectd in Debian-like systems.

#### Requirements

 * `git-core` (will be installed)
 * `collectd` (will not be installed)

#### Variables

* `collectd_plugin_haproxy_version`: [default: `v1.0.1`]: Version to install (e.g. `master`)

* `collectd_plugin_haproxy_socket`: [default: `/var/run/haproxy.sock`]: Stats socket to get data from
* `collectd_plugin_haproxy_proxy_monitors`: [default: `['frontend', 'backend', 'server']`]: Proxy monitors

#### Dependencies

None

#### Example(s)

##### Simple

```yaml
---
- hosts: all
  roles:
    - collectd-plugin-haproxy
```

##### Advanced

```yaml
---
- hosts: all
  roles:
    - collectd-plugin-haproxy
  vars:
    collectd_plugin_haproxy_version: master
    collectd_plugin_haproxy_socket: /run/haproxy/admin-1.sock
    collectd_plugin_haproxy_proxy_monitors:
      - frontend
      - backend
      - server
      - socket/listener
```

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-collectd-plugin-haproxy/issues)!
