# ansible-collectd

An Ansible role for installing [Collectd](http://collectd.org).

## Role Variables

- `collectd_version` - Collectd version
- `collectd_interval` - Collectd metrics collection interval (default: `10`)
- `collectd_load_plugins` - Collectd plugins to load (see [defaults](./defaults/main.yml))

## Example Playbook

By default, this role does not load any Collectd plugins. Most likely, you will want some plugins enabled in order to collect metrics.

In order to use any Collectd plugins with this role, simply list the plugins you want enabled as a list via `collectd_load_plugins`. Then, generate templates for each plugin configuration file and place the rendered template in `/etc/collectd/collectd.conf.d`.

See the `azavea.graphite` [examples](https://github.com/azavea/ansible-graphite/tree/develop/examples) directory for a more complete example.
