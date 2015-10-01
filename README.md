# Docker cELK stack

Run the cELK (collectd, Elasticseach, Logstash, Kibana) stack with Docker and Docker-compose.

Based on the official images:

* [elasticsearch](https://registry.hub.docker.com/_/elasticsearch/)
* [logstash](https://registry.hub.docker.com/_/logstash/)
* [kibana](https://registry.hub.docker.com/_/kibana/)

And unofficial ..

* [collectd](https://hub.docker.com/r/yaronr/collectd/)

# Requirements

## Setup

1. Install [Docker](http://docker.io).
2. Install [Docker-compose](http://docs.docker.com/compose/install/).
3. Clone this repository

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

By default, the stack exposes the following ports:
* 5000: Logstash TCP input.
* 9200: Elasticsearch HTTP (with Marvel plugin accessible via [http://localhost:9200/_plugin/marvel](http://localhost:9200/_plugin/marvel))
* 5601: Kibana 4 web interface
