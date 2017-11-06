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

.. code::

  cd <git clone directory>/json/ **got clone directory from Lab 1**
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

   |template1|

#. You should now see a collection named 'F5 ELK'
   in your Postman Collections sidebar:

   |template2|

#. Import the Environment file by clicking 'Import' -> 'Import from Link' and
   pasting the following URL and clicking 'Import':

   .. parsed-literal:: 

      :raw_github_url:`/postman_collections/F5 ELK Env.postman_environment.json` 


.. |template1| image:: /_static/template1.png
   :width: 12.0in
   :height: 3.0in
.. |template2| image:: /_static/template2.png
   :width: 12.0in
   :height: 3.0in


#. 