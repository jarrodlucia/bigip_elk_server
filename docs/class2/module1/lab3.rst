.. |labmodule| replace:: 1
.. |labnum| replace:: 3
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Install Kibana
--------------------------------------------

In this lab we will install Kibana

Task 1 Install Kibana
~~~~~~~~~~~~~~~~~~~~~

#. Install Kibana

	.. code::

	  sudo apt-get install kibana

#. Change config file to set Outside IP address

	.. code::

	  sudo vi /etc/kibana/kibana.yml


.. NOTE::

	Kibana is served by a back end server. This setting specifies the port to use. Server port is set as default Kibana Port 5601. Server host should be set to the UDF Management IP address 10.1.1.5 as we will be accessing this via the Linux Jumphost. The URL of the Elasticsearch instance to use for all your queries.

	- server.port: 5601
	- server.host: "10.1.1.5"
	- elasticsearch.url: "http://localhost:9200"

|kibana1|


.. |kibana1| image:: /_static/kibana1.png
   :width: 3.5in
   :height: 2.0in


#. Kibana restart

	.. code::

	  sudo systemctl restart kibana.service


#. To configure Kibana to start automatically when the system boots up, run the following commands:

	.. code::

	  sudo /bin/systemctl daemon-reload
	  sudo /bin/systemctl enable kibana.service


#. Kibana Control

	.. code::

	  sudo systemctl start kibana.service
	  sudo systemctl stop kibana.service


#. Check Kibana is running via command-line:

|kibana2|


.. |kibana2| image:: /_static/kibana2.png
   :width: 3.5in
   :height: 2.0in


#. Access Kibana via Linux Jumpbox to verify access


|kibana3|


.. |kibana3| image:: /_static/kibana3.png
   :width: 3.5in
   :height: 2.0in


