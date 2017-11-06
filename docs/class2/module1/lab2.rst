.. |labmodule| replace:: 1
.. |labnum| replace:: 2
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Install Elasticsearch
---------------------------------------------------

This lab will install the Elasticsearch component, It is recommended to install Elasticsearch as the first module.

Task 1 Install Repo and Keys
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Download and install the public signing key:

..code::

	wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -

#. Save the repository definition to /etc/apt/sources.list.d/elastic-5.x.list:

..code::
	echo "deb https://artifacts.elastic.co/packages/5.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-5.x.list
	sudo apt-get update

Task 2 Install elasticseach and setup system
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Install Elasticsearch

..code::

	sudo apt-get install elasticsearch

#. Edit config file to change bind address

..code::
	
	sudo vi /etc/elasticsearch/elasticsearch.yml

	Set bind to localhost
	# ---------------------------------- Network -----------------------------------
	#
	# Set the bind address to a specific IP (IPv4 or IPv6):
	#
	network.host: localhost

#. Restart Elastic Search

..code::
	
	sudo systemctl restart elasticsearch

#. Configure the system to start at boot

..code::
	
	sudo /bin/systemctl daemon-reload
	sudo /bin/systemctl enable elasticsearch.service

#.	Checking Start / Stop / Status

..code::

	sudo systemctl start elasticsearch.service
	sudo systemctl stop elasticsearch.service
	sudo systemctl status elasticsearch.service
