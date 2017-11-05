.. |labmodule| replace:: 1
.. |labnum| replace:: 5
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Configure elasticsearch templates
---------------------------------------------------------------

Upload elasticsearch templates and mappings



Task 1 - Curl module templates inot elasticsearch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#Install Index Templates into Elastic Search for the required modules
- CURL - XPUT *.json (requried file upload)
- curl -XPUT http://localhost:9200/_template/pem?pretty -d @pem_mapping.json
- curl -XPUT http://localhost:9200/_template/afm?pretty -d @afm_mapping.json
- curl -XPUT http://localhost:9200/_template/dns?pretty -d @dns_mapping.json


We will implement a workflow that is best depicted by the following branch
diagram:

.. code::

   Start
     |
     |- Authenticate
     |  |- Authenticate to BIG-IP A
     |  |- Authenticate to BIG-IP B
     |
     |- Get BIGIP Version
     |  |- Get BIGIP Version on BIG-IP A
     |  |- Get BIGIP Version on BIG-IP B
     |
   Stop

T