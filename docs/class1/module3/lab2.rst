.. |labmodule| replace:: 2
.. |labnum| replace:: 2
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Create and Modify AVR Widgets
-----------------------------------------------------------

AVR dashbaords are customisable. This is accomplished via adding
changing and removing widgets.

Task 1 – Create a new widget
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perform the following steps to complete this task:

#. Click the “Step 1: Discover BIGIP-A Device” item in the Postman
   collection. This will request will perform a POST to the
   ``/mgmt/shared/resolver/device-groups/cm-cloud-managed-devices/devices``
   worker to perform the device discovery process. Examine the JSON body
   so you understand what data is sent to perform the discovery process:

   |image51|


#. Click the “Step 2: Discover BIGIP-B Device” item in
   the collection.

#. Click the “Step 3: Get Discovered Devices” item in the collection.
   We will GET the devices collection and verify that both BIG-IP
   devices show a ‘state’ of ‘ACTIVE’:

   |image55|

.. |image51| image:: /_static/image051.png
   :scale: 40%
.. |image52| image:: /_static/image052.png
   :width: 5.21233in
   :height: 2.73647in