.. |labmodule| replace:: 1
.. |labnum| replace:: 7
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Create Index and Import Pre-Configured
--------------------------------------------------------------------

This Lab will focus on creating the index's for each module based on logstash in **Lab4**

We will import the prepared f5 module json kibana searches / virtuals / and dashboards.


Task 1 - Create Kibana Index's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Configure Indexes in Kibana

Configure the first and default index

- index pattern = ``pem-*``
- select ``@timestamps``

|template15|

.. |template15| image:: /_static/template15.png
   :width: 12.0in
   :height: 5.0in


- index pattern = ``afm-*``
- select ``@timestamps``

**Follow PEM example above for AFM**

- index pattern = ``dns-*``
- select ``@timestamps``

|template14|

.. |template14| image:: /_static/template14.png
   :width: 12.0in
   :height: 5.0in


Task 2 - Import preconfigured Kibana json's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Searches / Visualisation and Dashboards

#. Import object data into Kibana

Import the JSON files in the following order:

- Searches
- Visualisations
- Dashboards

**Searches**

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_searches.json`

|template10|

.. |template10| image:: /_static/template10.png
   :width: 12.0in
   :height: 5.0in

|template11|

.. |template11| image:: /_static/template11.png
   :width: 4.0in
   :height: 3.0in

**Visuals**

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_visualisations.json`

|template12|

.. |template12| image:: /_static/template12.png
   :width: 6.0in
   :height: 5.0in

**Dashboards**

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_dashboards.json`

|template13|

.. |template13| image:: /_static/template13.png
   :width: 12.0in
   :height: 6.0in

.. NOTE::

	**The JSON files have been placed in the IN_CASE_OF_EMERGENCY folder on the desktop**

