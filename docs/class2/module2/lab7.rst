.. |labmodule| replace:: 2
.. |labnum| replace:: 7
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Create Index and Import templates
---------------------------------------------------------------

create index's in kibana

import f5 module json searches / virtuals / dashboards


Task 1 - Create Kibana Index's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

# Configure Indexes in Kibana
#Configure Indexes in Kibana
- index pattern = pem-*
- select @timestamps

- index pattern = afm-*
- select @timestamps

- index pattern = dns-*
- select @timestamps


Task 2 - Import preconfigured Kibana json's
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

# Searches / Visualisation and Dashboards
#Import object data into Kibana
- Change Index UUID in json
- Import object json into Kibana