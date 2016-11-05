# POC Nifi (cluster) and Zookeeper integration with Docker

This POC is using Docker image from [nifi-docker-cluster](https://github.com/thuongdinh/nifi-docker-cluster).

## Target
 - Run HDFS, Spark and Jupyter Notebook with docker/docker-compose
 - Note: Spark cluster will run standalone mode (not support YARN or Mesos)

## Requirements
 - Docker version 1.12.3
 - Docker Compose version 1.8.1

## Basic docker up

1. Up docker-compose

	```
	$ docker-compose up -d
	```

2. Browse Web UI for components:
 - Apache Nifi: http://localhost:8080/nifi/

3. Template
 - pull-from-twitter-farden-hose.xml: this flow demonstrates how to config twitter streaming.
 - simple-httpget-route.xml: this flow demonstrates how to crawl a web server and save result to file.

## Known Issues
 - Cannot use docker-compose scale for nifi-nodes, assuming can solve this issue when deploy to multiple host.