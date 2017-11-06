.. |labmodule| replace:: 1
.. |labnum| replace:: 7
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Create Index and Import Pre-Configured
--------------------------------------------------------------------

create index's in kibana

import f5 module json searches / virtuals / dashboards


Task 1 - Create Kibana Index's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Configure Indexes in Kibana
- index pattern = pem-*
- select @timestamps

- index pattern = afm-*
- select @timestamps

- index pattern = dns-*
- select @timestamps


Task 2 - Import preconfigured Kibana json's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

# Searches / Visualisation and Dashboards

#. Import object data into Kibana

add screen of import

Searches

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_searches.json`

Visuals

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_visualisations.json`

Dashboards

   .. parsed-literal:: 

      :raw_github_url:`/json/elk_dashboards.json`