.. |labmodule| replace:: 1
.. |labnum| replace:: 2
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Install Elasticsearch
---------------------------------------------------

In this lab we will install elasticsearch

Task 1 Install repo and keys
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#Download and install the public signing key:
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -

#Save the repository definition to /etc/apt/sources.list.d/elastic-5.x.list:
echo "deb https://artifacts.elastic.co/packages/5.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-5.x.list

sudo apt-get update

Task 2 Install elasticseach and setup system
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#Install
sudo apt-get install elasticsearch

#Edit config file to change bind address
sudo vi /etc/elasticsearch/elasticsearch.yml

Set bind to localhost
# ---------------------------------- Network -----------------------------------
#
# Set the bind address to a specific IP (IPv4 or IPv6):
#
network.host: localhost

#Restart Elastic Search
sudo systemctl restart elasticsearch

#Start at boot
sudo /bin/systemctl daemon-reload
sudo /bin/systemctl enable elasticsearch.service

#Checking Start / Stop / Status
sudo systemctl start elasticsearch.service
sudo systemctl stop elasticsearch.service
sudo systemctl status elasticsearch.service
