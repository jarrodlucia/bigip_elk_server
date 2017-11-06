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

RECOMMENDAION - use cURL for the uploading of the templates with json file. POSTMAN is useful for Elasticsearch management once the template are in place.



Task 1 - Install module templates in Elasticsearch via cURL
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#Install Index Templates into Elastic Search for the required modules

.. code::

  curl -XPUT http://localhost:9200/_template/pem?pretty -d @pem_mapping.json
  curl -XPUT http://localhost:9200/_template/afm?pretty -d @afm_mapping.json
  curl -XPUT http://localhost:9200/_template/dns?pretty -d @dns_mapping.json


