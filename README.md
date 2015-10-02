# Docker cELK stack

|Service  | Base Image | Port |
|--------:|:----------:|:----:|
|[collectd](https://collectd.org/)|[:link:](https://hub.docker.com/r/yaronr/collectd/)|25826/udp||
|[logstash](https://www.elastic.co/products/logstash)|[:link:](https://registry.hub.docker.com/_/logstash/)|5000||
|[elasticsearch](https://www.elastic.co/products/elasticsearch)|[:link:](https://registry.hub.docker.com/_/elasticsearch/)|9200||
|[kibana](https://www.elastic.co/products/kibana)|[:link:](https://registry.hub.docker.com/_/kibana/)|5601||

# Setup

1. Install [Docker](http://docker.io).
2. Install [Docker Compose](http://docs.docker.com/compose/install/).
3. `git clone git@github.com:codenamekt/celk-docker-compose.git`

# Usage

Start the stack using *docker-compose*:

```bash
$ docker-compose up
```

You can also choose to run it in background (detached mode):

```bash
$ docker-compose up -d
```

When the stack starts you will immediately start seeing stats from collectd get pushed into the ELK stack via collectd. Stats like cpu, memory and load.

Access Kibana UI by hitting [http://localhost:5601](http://localhost:5601) with a web browser to view the statistics.

![Kibana](screenshot.png?raw=true "Kibana")

# Thanks

* [Elastic](https://www.elastic.co)
* [deviantony/docker-elk](https://github.com/deviantony/docker-elk)
