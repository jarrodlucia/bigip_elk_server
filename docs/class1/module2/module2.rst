Module 2: F5 Application Visibility and Reporting
=================================================

In this module we will explore how to configure and use F5’s Application Visibility and Reporting to provide application reporting. Analytics (also called Application Visibility and Reporting) is a module on the BIG-IP® system that you can use to analyze the performance of services and applications. It provides detailed metrics such as transactions per second, server and client latency, request and response throughput, and sessions. You can view metrics for applications, virtual servers, pool members, URLs, specific countries, and additional detailed statistics about application traffic running through the BIG-IP system.

The labs in the module will focus on the high level features of AVR. 
These will include Analytics profiles, configuration and navigation of the AVR 
reports and information generated.

The BIG-IP in the lab is preconfigured with DNS / PEM / and AFM provisioned and configured. Please explore the current f5 config to familarise yourself with this lab.

Confirm the following main config items to verify your BIG-IP lab is on working order:

# Checked Provisioned Modules refelcts the below image (DNS / PEM / AFM and AVR).

|prov_image|

# Check VLAN setup. Make sure Interval VLAN is set to source (SP DAG).

|vlans| |vlan_dag|

# Verify SELF-IP's and routes are present.

|self_ip|	|routes|

# Check that PeM Data plane is setup, you should see four PEM data plane VS as below.

|pem_data_plane|

# Check that DNS Listener is configured.

|sp_dns|

.. NOTE::
	Explore the rest of the configuration. Please look at the DNS setup (cache / monitor) and AFM CGNAT (NAPT) configurations.

.. |prov_image| image:: /_static/prov_image.png
   :scale: 80%
.. |vlans| image:: /_static/vlan.png
   :scale: 80%
.. |vlan_dag| image:: /_static/vlan_dag.png
   :scale: 80%
.. |self_ip| image:: /_static/self_ip.png
   :scale: 80%
.. |routes| image:: /_static/routes.png
   :scale: 80%
.. |pem_data_plane| image:: /_static/pem_data_plane.png
   :scale: 80%
.. |sp_dns| image:: /_static/sp_dns.png
   :scale: 80%

.. toctree::
   :maxdepth: 1
   :glob:

   lab*