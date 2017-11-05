.. |labmodule| replace:: 2
.. |labnum| replace:: 2
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Access Clients and Generate Traffic
-----------------------------------------------------------------

In this lab you will walk through re-configuring the Clients to USE the F5 for traffic. This will generate traffic for PEM / DNS / and AFM for AVR and logging to ELK Stack.

Task 1 - Configure Client Netwoking & Traffic Generation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In this task we will configure and use the Client UDF machines. These Clients are required to be reconfigured to utilise the network and DNS from the F5.. 

Perform the following steps to complete this task:

#. Click the on the RDP access for UDF for each client.

	|rdp_access|

	Accept warning allways

	|rdp_accept|

#. Click on the networking script (this will prompt for Sudo password)

    |net_script|

#. Once the script has completed, check netstat -nr and nslookup to verify you have traffic passing the F5.

    |netstat|

#. Verify in BIG-IP TMUI that you see traffic on the F5 VS's

    |verify_traffic|

#. Apply the same fix for the other client.

#. Once both clients are fixed, generate traffic by opening applications and webpages (Leave the applications open so traffic generation continues)

    |traffic_gen|

.. |rdp_access| image:: /_static/rdp_access.png
   :width: 7.0in
   :height: 5.0in
.. |rdp_accept| image:: /_static/rdp_accept.png
   :width: 7.0in
   :height: 5.0in
.. |net_script| image:: /_static/net_script.png
   :width: 7.0in
   :height: 5.0in
.. |netstat| image:: /_static/netstat.png
   :width: 7.0in
   :height: 5.0in
.. |verify_traffic| image:: /_static/verify_traffic.png
   :width: 7.0in
   :height: 5.0in
.. |traffic_gen| image:: /_static/traffic_gen.png
   :width: 7.0in
   :height: 5.0in