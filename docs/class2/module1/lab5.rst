.. |labmodule| replace:: 1
.. |labnum| replace:: 5
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Configure elasticsearch templates
---------------------------------------------------------------

Upload elasticsearch templates and mappings. There are multiple way this can be achieved. The most common ways are cURL and a REST based program such as POSTMAN. Feel free to use whichever method you are most comfortable with.

.. NOTE:: 

    **RECOMMENDATION** Use cURL for the uploading of the templates with json file. POSTMAN is useful for Elasticsearch management once the template are in place.


Task 1 Option1 - Install module templates in Elasticsearch via cURL
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Install Index Templates into Elastic Search for the required modules

  cd <git clone directory>/json/ **git clone directory from Lab 1**

.. code::

  curl -XPUT http://localhost:9200/_template/pem?pretty -d @pem_mapping.json
  curl -XPUT http://localhost:9200/_template/afm?pretty -d @afm_mapping.json
  curl -XPUT http://localhost:9200/_template/dns?pretty -d @dns_mapping.json


Task 1 Option1 - Install module templates in Elasticsearch via POSTMAN
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Import ELK Postman Collection and Environment

#. Click the 'Import from Link' tab.  Paste the following URL into the
   text box and click 'Import'

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/ELK Stack.postman_collection.json`


#. You should now see a collection named 'F5 ELK'
   in your Postman Collections sidebar:

   |template1|

#. Import the Environment file by clicking 'Import' -> 'Import from Link' and
   pasting the following URL and clicking 'Import':

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/F5 ELK Env.postman_environment.json` 

   |template2|


.. |template1| image:: /_static/template1.png
   :width: 6.0in
   :height: 5.0in
.. |template2| image:: /_static/template2.png
   :width: 2.0in
   :height: 1.0in


#. Click on GET Elasticsearch information, **HIT SEND**.

|template3|

.. |template3| image:: /_static/template3.png
   :scale 80%


You should see cluster information regarding elasticsearch


#. Click on GET Elasticsearch indices, **HIT SEND**.

|template4|

.. |template4| image:: /_static/template4.png
   :width: 6.0in
   :height: 5.0in


You should see the current index's and information regarding each index.

**We will use this command to observe the creation of new indexes**


#. Click on GET Elasticsearch Template Searches, **HIT SEND**

|template5|

.. |template5| image:: /_static/template5.png
   :width: 6.0in
   :height: 5.0in


You should see any current templates listed.

.. NOTE::
    New Install will **NOT** contain any templates showing {}


#. Click on Create Template AFM + PEM + DNS **Install all templates**

|template6|

.. |template6| image:: /_static/template6.png
   :width: 6.0in
   :height: 5.0in


.. NOTE::
    Create all templates from the POSTMAN collection


#. Verify templates created and exist. Click on GET Elasticsearch Template Searches

|template7|

.. |template7| image:: /_static/template7.png
   :width: 6.0in
   :height: 5.0in


.. NOTE::
    Look through the template JSON outputted by POSTMAN. Verify and check that the three templates created are present.

