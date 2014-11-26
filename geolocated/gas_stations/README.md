geographic dataset
======================

# Content

List of all gas stations in France (10952 elements).

Original file can be found [here](https://www.data.gouv.fr/fr/datasets/stations-services-en-france)

## Files

* gas_stations.csv : data file
* logstash.conf : logstash configuration
* mapping.json : mapping of the type `gas_stations`

## How to

1. Update the logstash config file : the file input `path` parameter must be set to the absolute path of the `gas_stations`.csv file
2. (Optional) by default, the data will be indexed in the `datasets` ElasticSearch index, under `gas_stations` type. Change the `elasticsearch_http` parameters `index` and `index_type` to whatever better suits your needs.
3. Create the `datasets` index :
    `curl -XPOST 'http://<your_host>:<your_port>/datasets'`
4. Add the `gas_stations` mapping :
    `curl -XPUT 'http://<your_host>:<your_port>/datasets/gas_stations/_mapping' -d @mapping.json'`
5. Launch logstash with (assuming you are in your logstash home folder):
    `bin/logstash -f logstash.conf`

# Purpose

The main interest of this dataset is that lat/lon of each station is indexed, allowing to play with **geolocation-related** queries and filters.
