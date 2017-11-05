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

#. You should now see a collection named 'F5 Automation & Orchestration Intro'
   in your Postman Collections sidebar:

   |image10|

#. Import the Environment file by clicking 'Import' -> 'Import from Link' and
   pasting the following URL and clicking 'Import':

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/F5 SPDevOps.postman_environment.json`

Task 2 – Configure TCP Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will create and configure TCP AVR profile and apply this to 
the requried VS.

Perform the following steps to complete this task:

#. Click the ‘Step 1: Get Authentication Token’ item in the Lab 2.1
   Postman Collection

#. Notice that we are sending a POST request to the
   ``/mgmt/shared/authn/login`` endpoint.

   |image41|

#
.. |image48| image:: /_static/image048.png
   :width: 4.67051in
   :height: 1.23217in
   

Task 3 – Configure PEM Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will create and configure TCP AVR profile and apply this to 
the requried VS.

Perform the following steps to complete this task:

#. Click the ‘Step 1: Get Authentication Token’ item in the Lab 2.1
   Postman Collection

#. Notice that we are sending a POST request to the
   ``/mgmt/shared/authn/login`` endpoint.

   |image41|


Task 4 – Configure AFM Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will create and configure TCP AVR profile and apply this to 
the requried VS.

Perform the following steps to complete this task:

#. Click the ‘Step 1: Get Authentication Token’ item in the Lab 2.1
   Postman Collection

#. Notice that we are sending a POST request to the
   ``/mgmt/shared/authn/login`` endpoint.

   |image41|

Task 5 – Configure DNS Analytics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this task we will create and configure TCP AVR profile and apply this to 
the requried VS.

Perform the following steps to complete this task:

#. Click the ‘Step 1: Get Authentication Token’ item in the Lab 2.1
   Postman Collection

#. Notice that we are sending a POST request to the
   ``/mgmt/shared/authn/login`` endpoint.



.. |image8| image:: /_static/image008.png
   :width: 0.46171in
   :height: 0.43269in
.. |image10| image:: /_static/image010.png
   :width: 3.54657in
   :height: 2.80000in
.. |image87| image:: /_static/image087.png
   :scale: 40%
.. |image88| image:: /_static/image088.png
   :scale: 40%