## ubuntu-1604-collectd-haproxy

Set up [SignalFx Collectd haproxy plugin](https://github.com/signalfx/collectd-haproxy) on Ubuntu 16.04.

#### Requirements

 * `collectd` (will not be installed, [see](https://github.com/mvdriel/ansible-ubuntu-1604-collectd))

#### Variables

 * `ubuntu_1604_collectd_haproxy_version`: [default: `v1.0.1`]: Version (tag) to install

 * `ubuntu_1604_collectd_haproxy_proxy_monitors`: [default: `['frontend', 'backend']`]: Proxy monitors
