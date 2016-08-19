Ansible Role: win_elasticsearch
===============================

[![Build Status](https://travis-ci.org/dohque/ansible-role-win-elasticsearch.svg?branch=master)](https://travis-ci.org/dohque/ansible-role-win-elasticsearch)

An Ansible Role that installs Elasticsearch on Windows.

Requirements
------------

Windows box should be prepared and configured to be accessible by Ansible.

<http://docs.ansible.com/ansible/intro_windows.html#windows-system-prep>

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
elasticsearch_version: "2.3.1"
```

Version of Elasticsearch to be installed.

```yaml
elasticsearch_cluster_name: elasticsearch
```

Elasticsearch will join cluster with this name.

```yaml
elasticsearch_network_host: 127.0.0.1
```

Network host to listen for incoming connections on. By default we only listen
 on the localhost interface. Change this to the IP address to listen on a
 specific interface, or 0.0.0.0 to listen on all interfaces.

```yaml
elasticsearch_http_port: 9200
```

The port to listen for HTTP connections on.

Dependencies
------------

  None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: dohque.win_elasticsearch }
```

Contributions
-------------

I will really appreciate any feedback and contributions. Feel free to contact me.

License
-------

MIT

Author Information
------------------

This role was created in 2016 by Ruslan Pilin.
