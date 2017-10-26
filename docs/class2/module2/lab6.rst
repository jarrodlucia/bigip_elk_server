.. |labmodule| replace:: 2
.. |labnum| replace:: 6
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Send Logs to ELK Stack
----------------------------------------------------

configure f5 for logging to new ELK stack

check that data is arriving at ELK stack


Task 1 - Set f5 to log to ELK Stack
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

# Prepare F5 for Logging
#Configure F5 BIG-IP to Send data
- Pool = tcp server:5514 - PEM
- Pool = tcp server:5515 - DNS
- Pool = tcp server:5516 - AFM/CGNAT

# Confirm Data on server and indexes
#Check that Data is arriving in the Index
curl 'localhost:9200/_cat/indices?v'
- health status index          uuid                   pri rep docs.count docs.deleted store.size pri.store.size
- yellow open   pem-2017.01.18 -drykpvETBK0wVN3dKTDxw   5   1        526            0      1.5mb          1.5mb
- yellow open   .kibana        da8KKtaLS12mpj9bm7Izig   1   1          1            0      3.1kb          3.1kb