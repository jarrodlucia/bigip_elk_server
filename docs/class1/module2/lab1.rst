.. |labmodule| replace:: 2
.. |labnum| replace:: 1
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Configure AVR Profiles
----------------------------------------------------

An Analytics profile is a set of definitions that determines the circumstances under which the system gathers, logs, notifies, and graphically displays information regarding traffic to an application or service. The Analytics module requires that you select an Analytics profile for each application you want to monitor. You associate the Analytics profile with one or more virtual servers used by the application / service. 

In the Analytics profile, you customize:
   -  What statistics to collect
   -  Where to collect data (locally, remotely, or both)
   -  Whether to capture the traffic itself
   -  Whether to send notifications.

Task 1 - Import the Postman Collection & Environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task you will Import a Postman Collection & Environment for this lab.
Perform the following steps to complete this task:

#. Open the Postman tool by clicking the |image8| icon of the desktop of
   your Linux Jumphost (Postman should be open from previous Lab)

#. Click the 'Import' button in the top left of the Postman window

|image87|

#. Click the 'Import from Link' tab.  Paste the following URL into the
   text box and click 'Import'

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/SP Modules.postman_collection.json`

  |image88|

.. |image8| image:: /_static/image008.png
   :width: 0.46171in
   :height: 0.43269in
.. |image87| image:: /_static/image087.png
   :scale: 40%
.. |image88| image:: /_static/image088.png
   :scale: 40%

#. You should now see a collection named 'SP Modules'
   in your Postman Collections sidebar:

   |postman_sp_mod|

#. Import the Environment file by clicking 'Import' -> 'Import from Link' and
   pasting the following URL and clicking 'Import':

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/F5 SPDevOps.postman_environment.json`

  |postman_sp_env|

.. |postman_sp_mod| image:: /_static/postman_sp_mod.png
   :width: 3.54657in
   :height: 2.80000in
.. |postman_sp_env| image:: /_static/postman_sp_env.png
   :width: 2.0in
   :height: 1.0in

Task 2 – Configure TCP Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will query and configure TCP AVR profile. This will be done using REST API (explored in previous Lab)

Perform the following steps to complete this task:

#. Click the ‘TCP Analytics’ item in the SP Module Postman Collection

#. Notice that we are sending a GET request to the ``/mgmt/tm/ltm/profile/tcp-analytics`` endpoint. Check the body returned and observer the default values.

    |get_tcp_profile|

#. Click on the 'Create TCP Analtics Profile' , check the body message for ELK_PEM_Publisher (We will use the PEM index in ELK for logging TCP Optimisation)

    |create_tcp_profile|

#. Verify in BIG-IP TMUI that the new profile was created.

    |verify_tcp_profile|

#. Add in the VS manually (This is not available in REST API currently)

    |add_tcp_vs|

.. |get_tcp_profile| image:: /_static/get_tcp_profile.png
   :width: 7.0in
   :height: 5.0in
.. |create_tcp_profile| image:: /_static/create_tcp_profile.png
   :width: 7.0in
   :height: 5.0in
.. |verify_tcp_profile| image:: /_static/verify_tcp_profile.png
   :width: 7.0in
   :height: 5.0in
.. |add_tcp_vs| image:: /_static/add_tcp_vs.png
   :width: 7.0in
   :height: 5.0in

Task 3 – Configure PEM Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will query and configure PEM AVR profile. This will be done using REST API (explored in previous Lab)

Perform the following steps to complete this task:

#. Click the ‘PEM’ item in the SP Module Postman Collection

#. Notice there are two sections we must update Global and Classification. We will do Global first, click on 'Request PEM Global Analytics Options' we are sending a GET request to the ``/mgmt/tm/pem/global-settings/analytics`` endpoint. Check the body returned and observer the default values.

    |get_pem_global|

#. Click on the 'Update PEM Global Analytics Options - External Logging' , check the body message for ELK_PEM_Publisher.

    |update_pem_global|

#. Verify in BIG-IP TMUI that the new updates where changed in PEM global options.

#. Click on 'Request PEM Classification Profile' we are sending a GET request to the ``/mgmt/tm/ltm/profile/classification/classification_pem`` endpoint. Check the body returned and observer the default values.

    |get_pem_class|

#. Click on the 'Update PEM Classification Profile' , check the body message for ELK_PEM_Publisher.

    |update_pem_class|

#. Verify in BIG-IP TMUI that the new updates where changed in PEM Classification.


.. |get_pem_class| image:: /_static/get_pem_class.png
   :width: 7.0in
   :height: 5.0in
.. |update_pem_class|image:: /_static/update_pem_class.png
   :width: 7.0in
   :height: 5.0in
.. |get_pem_global| image:: /_static/get_pem_global.png
   :width: 7.0in
   :height: 5.0in
.. |update_pem_global|image:: /_static/update_pem_global.png
   :width: 7.0in
   :height: 5.0in

Task 4 – Configure AFM Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will query and configure AFM AVR profile and Logging. This will be done using REST API (explored in previous Lab)

Perform the following steps to complete this task:

#. Click the ‘AFM’ item in the SP Module Postman Collection

#. Notice there are two sections we must update Security Reporting and Event Logging. We will do Security Reporting first, click on 'Request AFM Security Reporting Settings' we are sending a GET request to the ``/mgmt/tm/security/analytics/settings`` endpoint. Check the body returned and observer the default values.

    |get_afm_report|

#. Click on the 'Update AFM Security Reporting Settings' , check the body message for ELK_AFM_Publisher.

    |update_afm_report|

#. Verify in BIG-IP TMUI that the new updates where changed in AFM Report Settings.

.. NOTE::
    Request AFM Device DoS Settings - Can be used to report on settings currently set, however REST API cannot be used to update these settings at this time.

#. Click on 'Request AFM Event Logger' we are sending a GET request to the ``/mgmt/tm/security/log/profile/`` endpoint. Check the body returned and observer the default values.

    |get_afm_log|

#. Click on the 'Create AFM Event Log Profile' , check the body message for ELK_AFM_Publisher.

    |create_afm_log|

#. Verify in BIG-IP TMUI that the new updates where changed in AFM Log.


.. |get_afm_report| image:: /_static/get_afm_report.png
   :width: 7.0in
   :height: 5.0in
.. |update_afm_report|image:: /_static/update_afm_report.png
   :width: 7.0in
   :height: 5.0in
.. |get_afm_log| image:: /_static/get_afm_log.png
   :width: 7.0in
   :height: 5.0in
.. |create_afm_log|image:: /_static/create_afm_log.png
   :scale 50%

Task 5 – Configure DNS Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will query and configure DNS AVR profile. This will be done using REST API (explored in previous Lab)

Perform the following steps to complete this task:

#. Click the ‘DNS’ item in the SP Module Postman Collection

#. Notice that we are sending a GET request to the ``/mgmt/tm/ltm/profile/dns-logging`` endpoint. Check the body returned and observer the default values.

    |get_dns_log|

#. Click on the 'Create DNS Log Profile' , check the body message for ELK_DNS_Publisher.

    |create_dns_log|

#. Verify in BIG-IP TMUI that the new profile was created.

.. |get_dns_log| image:: /_static/get_dns_log.png
   :width: 7.0in
   :height: 5.0in
.. |create_dns_log| image:: /_static/create_dns_log.png
   :width: 7.0in
   :height: 5.0in