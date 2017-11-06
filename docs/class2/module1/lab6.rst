.. |labmodule| replace:: 1
.. |labnum| replace:: 6
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Send Logs to ELK Stack
----------------------------------------------------

configure f5 for logging to new ELK stack

check that data is arriving at ELK stack


Task 1 - Confirm BIG-IP is sending logs to ELK Stack
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Confirm via TMUI that the setup from **Class 1 Lab 2.1** 

add in screens


.. NOTE:: 

	Make sure the correct port is allocated as per previous Logstash configuration
		- Pool = tcp server:5514 - PEM
		- Pool = tcp server:5515 - DNS
		- Pool = tcp server:5516 - AFM/CGNAT


#. Confirm Data is arrinving on server

.. code::

sudo tcpdump -i eth1 port 5514


#. Check that Data is arriving in the Index

curl 'localhost:9200/_cat/indices?v'

|template8|

.. |template8| image:: /_static/template8.png
   :width: 5.0in
   :height: 7.0in


or via POSTMAN

|template9|

.. |template9| image:: /_static/template9.png
   :width: 6.0in
   :height: 5.0in