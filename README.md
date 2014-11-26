elasticsearch-datasets
======================

Datasets created to play with ElasticSearch, for various use cases.

# Features

For each dataset, you will find :
* the csv file with the data itself
* a logstash configuration file to process this data file with logstash and send it to your cluster (localhost by default)
* the json file of the related mapping for your cluster to process the data accordingly

Each dataset has been tested with the following versions of the ELK stack :
* ElasticSearch 1.3.2+
* Logstash 1.4.0+

# Use cases

* [geolocated data](geolocated)
* [names, strings](strings)