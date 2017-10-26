.. |labmodule| replace:: 2
.. |labnum| replace:: 1
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Explore AVR Dashboards
----------------------------------------------------

With AVR provisioned and AVR profiles configured, prebuilt
dashboards will begin to display data.

Task 1 – BIG-IP Performance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will observe the performance AVR report and change
the timescale.

For more information about external authentication providers see the
section titled “\ **About external authentication providers with
iControl REST**\ ” in the iControl REST API User Guide available at
https://devcentral.f5.com

Perform the following steps to complete this task:

#. Click the ‘Step 1: Get Authentication Token’ item in the Lab 2.1
   Postman Collection

#. Notice that we are sending a POST request to the
   ``/mgmt/shared/authn/login`` endpoint.

   |image41|

#. Click the ‘Body’ tab and examine the JSON that we will send to
   iWorkflow to provide credentials:

   |image42|

#. Modify the JSON body and add the required credentials (admin/admin).
   Then click the ‘Send’ button.



   |image50|

.. |image41| image:: /_static/image041.png
   :scale: 40%
.. |image42| image:: /_static/image042.png

