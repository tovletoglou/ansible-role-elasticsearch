# Ansible Role: ElasticSearch

Installs ElasticSearch on Centos 7

## Requirements

- Tested CentOS 7
- You need Java >= 1.8.0

## Role Variables

For ElasticSearch 5.1.1 the minimum java version is 1.8.0

```
elasticsearch_minimum_java_version: 1.8.0
```

Packages will be installed.

```
elasticsearch_tools:
  - elasticsearch
  - kibana
  # - filebeat
  # - logstash
  # - metricbeat
  # - packetbeat
```

The default host is the `localhost`. Change it to an IP in order to access it externally.

```
elasticsearch_host: localhost
```

The default port is `9200`. Change it if you a facing a conflict.

```
elasticsearch_port: 9200
```

Kibana is served by a back end server. This setting specifies the port to use.

```
elasticsearch_kibana_port: 5601
```

Specifies the address to which the Kibana server will bind. IP addresses and host names are both valid values. The default is 'localhost', which usually means remote machines will not be able to connect. To allow connections from remote users, set this parameter to a non-loopback address.

```
elasticsearch_kibana_host: localhost
```

The Kibana server's name. This is used for display purposes.

```
elasticsearch_kibana_name: kibana-name
```

The URL of the ElasticSearch instance to use for all your queries.

```
elasticsearch_kibana_bind_url: "http://localhost:9200"
```

Kibana uses an index in ElasticSearch to store saved searches, visualizations and dashboards. Kibana creates a new index if the index doesn't already exist.

```
elasticsearch_kibana_index: .kibana
```

## Dependencies

## License

MIT

## Author Information

Apostolos Tovletoglou [ansible-role-elasticsearch](https://github.com/tovletoglou/ansible-role-elasticsearch)
