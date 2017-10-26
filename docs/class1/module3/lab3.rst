.. |labmodule| replace:: 2
.. |labnum| replace:: 3
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: AVR Report Management - Export
------------------------------------------------------------

This lab will have you configure a customer report, and export
to pdf. This can be done at timed intervals.
 
Task 1 – Create / Re-use custom dashboard from Lab 2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Chose the AVR report you want to export.

Perform the following steps to complete this task:

#. Expand the “Lab 2.3 – Create Tenant & Local Connector” folder in the Postman
   collection.



Task 2 - Export Report
~~~~~~~~~~~~~~~~~~~~~~

#. Click the “Step 4: Create a Local Connector” item in the
   collection. We will create a new connector by performing a POST to
   the local connector collection. If you examine the JSON body you
   can see we are providing a reference to the URL for the BIG-IP-A
   device (using the UUID environment variable we populated earlier):

   |image56|

#. Click the “Step 6: Assign Connector to Tenant” item in the
   collection. This request will assign this connector to
   to the ‘MyTenant’ tenant allowing service deployments from that
   tenant. Click the ‘Send’ button and examine the response.

.. |image56| image:: /_static/image056.png
   :scale: 40%
.. |image57| image:: /_static/image057.png
   :width: 5.24968in
   :height: 2.77172in
.. |image58| image:: /_static/image058.png
   :scale: 40%
