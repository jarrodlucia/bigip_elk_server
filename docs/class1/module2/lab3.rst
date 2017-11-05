.. |labmodule| replace:: 2
.. |labnum| replace:: 3
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Navigating AVR
--------------------------------------------

Navigating and viewing AVR reports.

Task 1 – BIG-IP Performance Report
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perform the following steps to complete this task:

#. Navigate to Performance Report under Statistics.

	|traffic_report|

	Explore the interface with the sliding bar, and tick and untick options.

.. |traffic_report| image:: /_static/traffic_report.png
   :width: 12.0in
   :height: 7.0in

Task 2 – AVR TCP Optimisation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perform the following steps to complete this task:

#. Navigate to Analytics TCP Statistics.

	|tcp_avr|

#. Explore the different display options by clicking around the dashboard.


	See the following link for further TCP AVR information:

	https://support.f5.com/kb/en-us/products/big-ip_analytics/manuals/product/analytics-implementations-12-1-0/9.html 


.. |tcp_avr| image:: /_static/tcp_avr.png
   :width: 12.0in
   :height: 5.0in

Task 3 – AVR Traffic Classification
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perform the following steps to complete this task:

#. Navigate to Traffic Classification Analytics.

	|avr_classification|

#. Explore the different display options by clicking around the dashboard.

.. |avr_classification| image:: /_static/avr_classification.png
   :width: 12.0in
   :height: 5.0in

Task 4 – PEM Analytics Report
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perform the following steps to complete this task:

#. Navigate to Policy Enforcement Analytics Overview.

	|pem_avr_overview|

#. Navigate to Policy Enforcement Analytics Statistics.

	|pem_avr_stats|

	Explore the different screens and options available for display. See the following link for further AVR information:

	https://support.f5.com/kb/en-us/products/big-ip-pem/manuals/product/pem-implementations-13-0-0.html 

.. |pem_avr_overview| image:: /_static/pem_avr_overview.png
   :width: 12.0in
   :height: 5.0in
.. |pem_avr_stats| image:: /_static/pem_avr_stats.png
   :width: 12.0in
   :height: 5.0in

Task 5 – Modify PEM AVR Dashboard / Export AVR Report
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will modify and add widgets to default dashboard, and export an Analytics dashboard to a PDF report.

Perform the following steps to complete this task:

#. Navigate to Policy Enforcement Analytics.

	|pem_avr_adjust|

#. Click on Add Widget

#. Create a New Wdiget of your choice.

#. Explore the options within the Dashboard widgets for display

#. Click on Export, select PDF to generate report.


.. |pem_avr_adjust| image:: /_static/pem_avr_adjust.png
   :width: 12.0in
   :height: 5.0in


Task 6 - PEM Scheduled Reports
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will configure a Scheduled PEM report.

Perform the following steps to complete this task:

#. Navigate to Policy Enforcement Analytics Scheduled Reports.

	|pem_sched_report|

#. Explore the options for scheduled reporting.


.. |pem_sched_report| image:: /_static/pem_sched_report.png
   :width: 7.0in
   :height: 7.0in