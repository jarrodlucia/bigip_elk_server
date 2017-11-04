Welcome
-------

Welcome to F5's Service Provider AVR and Big Data hands on training series.
The intended audience for these labs are Service Provider engineers that
would like to leverage the power of F5 data visibility and integrate this
immense data capability into open source tools such as Elasticsearch, Hadoop
and others.


Getting Started
---------------

Please follow the instructions provided by this documentation to start your
lab and access your lab.

.. NOTE::
	All work for this lab will be performed exclusively from the Linux Jumphost
  and Linux Client Machines. All required access and servies needed to perform
  classes and labs are provided by the UDF. No installation or interaction with your local 
  system is required.

Prerequisits
----------------

In order to complete this series of training classes you will need to utilize
the provided blueprint for the course session. To access the UDF sessions you will
need to have the following prerequists met. 

- Current Access to UDF
- SSH key of your access machine in UDF
- Windows or MAC ssh client working with UDF


All pre-built environments implement the :ref:`lab-topology` shown below.

UDF Blueprint
~~~~~~~~~~~~~~~~~

Please follow the instructions provided by your lab instructor to access your
lab environment. The lab environment will be delivered  via UDF blueprints to 
each student.

.. NOTE:: Please deploy and start your lab as soon as you have access to the class
the lab takes some time to boot all the components.


Lab Topology
------------

The network topology implemented for this lab based on the Service Provider Gi lan
path. The focus of the lab is Control Plane programmability and Data Plane elements,
so this lab will focus at both parts at different time.
The following components have been included in your lab environment:

-  1 x F5 BIG-IP VE (v13.0 HF2)

-  1 x Linux Jumphost (ubuntu 16.04 - mate)

-  2 x Linux Clients (ubuntu 16.04 - mate)

-  1 x Linux Server (ubuntu 16.04)

.. _lab-topology:

Insert diagram here


The following table lists VLANS, IP Addresses and Credentials for all
components:

.. csv-table:: Lab Network Information
    :header: "Component", "IP Address", "Credentials"
    :widths: 40, 40, 60

    "Linux Jumphost", "10.1.1.20", "needtoadd"
    "BIG-IP Internal", "10.1.10.5", "admin/admin"
    "BIG-IP External", "10.1.20.5", "^"
    "BIG-IP Control", "10.1.30.5", "^"
    "Client 00 Mgmt", "10.1.1.9", "udfclient/S3rv1ceP0weR"
    "Client 00 Net", "10.1.10.25", "^"
    "Client 01 Mgmt", "10.1.1.7", "udfclient/S3rv1ceP0weR"
    "Client 01 Net", "10.1.10.30", "^"