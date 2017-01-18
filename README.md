# BIG-IP ELK Server Install
Setup for elk Server setup for BIG-IP logging

# Base Install
install completed on LXC Ubuntu 16.04
- ubuntu_lxc_base file for base setup
  
#Elastic Search Setup
- ubuntu_lxc_elastic_install

#Kibana Install and Server setup
- ubuntu_lxc_kibana

#Logstash Install
- ubuntu_lxc_logstash

#Install PEM Index into Elastic Search
- Use curl file

#Configure F5 BIG-IP to Send data
Pool = tcp server:5514

#Check that Data is arriving in the Index
curl 'localhost:9200/_cat/indices?v'
health status index          uuid                   pri rep docs.count docs.deleted store.size pri.store.size
yellow open   pem-2017.01.18 -drykpvETBK0wVN3dKTDxw   5   1        526            0      1.5mb          1.5mb
yellow open   .kibana        da8KKtaLS12mpj9bm7Izig   1   1          1            0      3.1kb          3.1kb

#Configure PEM Index in Kibana
- index pattern = pem-*
- select @timestamps
