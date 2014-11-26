elasticsearch-datasets
======================

Datasets created to play with ElasticSearch, for various use cases.

# Features

For each dataset, you will find :
* the csv file with the data itself
* configuration file for Logstash to ingest the data file
* the json file of the related mapping for your cluster to process the data accordingly

# Prerequisites

## Softwares
You will need :
* Logstash to parse the data file
* (obviously) a running ElasticSearch cluster where to index the data

## About versions
Each dataset has been tested with the following versions of the ELK stack :
* ElasticSearch 1.3.2+
* Logstash 1.4.0+

But both configurations (ElasticSearch type mapping and Logstash config) are using quite established features,
so feel free to try using older versions.

# Use cases

* [geolocated data](geolocated)
* [names, strings](strings)