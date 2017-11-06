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


..NOTE:: 

	Make sure the correct port is allocated as per previous Logstash configuration
		- Pool = tcp server:5514 - PEM
		- Pool = tcp server:5515 - DNS
		- Pool = tcp server:5516 - AFM/CGNAT


#. Confirm Data is arrinving on server

.. code::

sudo tcpdump -i eth1 port 5514


#. Check that Data is arriving in the Index

curl 'localhost:9200/_cat/indices?v'

- health status index          uuid                   pri rep docs.count docs.deleted store.size pri.store.size
- yellow open   pem-2017.01.18 -drykpvETBK0wVN3dKTDxw   5   1        526            0      1.5mb          1.5mb
- yellow open   .kibana        da8KKtaLS12mpj9bm7Izig   1   1          1            0      3.1kb          3.1kb


or Postman screenshot