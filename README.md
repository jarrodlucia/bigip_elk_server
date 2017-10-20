# BIG-IP ELK Server Install
Setup for elk Server setup for BIG-IP logging

# Base Install
install completed on LXC Ubuntu 16.04
- ubuntu_base_install file for base setup

# Elasticsearch Install
#Elastic Search Setup
- ubuntu_elastic_install

# Kibana Install
#Kibana Install and Server setup
- ubuntu_kibana

# Logstash Install
#Logstash Install
- ubuntu_logstash

#Additional Plug-ins
- sudo /usr/share/logstash/bin/logstash-plugin install logstash-filter-geoip
- sudo /usr/share/logstash/bin/logstash-plugin install logstash-filter-dns

# Prepare Elasticsearch templates
#Install Index Templates into Elastic Search for the required modules
- CURL - XPUT *.json (requried file upload)
- curl -XPUT http://localhost:9200/_template/pem?pretty -d @pem_mapping.json
- curl -XPUT http://localhost:9200/_template/afm?pretty -d @afm_mapping.json
- curl -XPUT http://localhost:9200/_template/dns?pretty -d @dns_mapping.json

# Prepare F5 for Logging
#Configure F5 BIG-IP to Send data
- Pool = tcp server:5514 - PEM
- Pool = tcp server:5515 - DNS
- Pool = tcp server:5516 - AFM/CGNAT

# Confirm Data on server and indexes
#Check that Data is arriving in the Index
curl 'localhost:9200/_cat/indices?v'
- health status index          uuid                   pri rep docs.count docs.deleted store.size pri.store.size
- yellow open   pem-2017.01.18 -drykpvETBK0wVN3dKTDxw   5   1        526            0      1.5mb          1.5mb
- yellow open   .kibana        da8KKtaLS12mpj9bm7Izig   1   1          1            0      3.1kb          3.1kb

# Configure Indexes in Kibana
#Configure Indexes in Kibana
- index pattern = pem-*
- select @timestamps

- index pattern = afm-*
- select @timestamps

- index pattern = dns-*
- select @timestamps

# Install and Configure NGINX
#Configure nginx for reverse proxy to Kibana


# Searches / Visualisation and Dashboards
#Import object data into Kibana
- Change Index UUID in json
- Import object json into Kibana
