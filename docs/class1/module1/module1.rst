Module 1: REST API Basics
=========================

In this module you will learn the basic concepts required to interact
with the BIG-IP iControl REST API. Additionally, you will walk through a
typical Device navigation.

This is a cut down version of the F5 Programmibility Super Net Ops training.

.. NOTE:: 
    The Lab Deployment for this lab includes a single BIG-IP devices.
    For most of the labs we will configuring the BIG-IP
    device (management IP and licensing have already been completed).
    BIG-IP-B already has some minimal configuration loaded.

.. NOTE::
    It’s beneficial to have GUI/SSH sessions open to BIG-IP devices while 
    going through this lab. Feel free to verify the actions taken in the lab 
    against the GUI or SSH. You can also watch the following logs:

    - BIG-IP:

      - /var/log/ltm
      
      - /var/log/restjavad.0.log

    - iWorkflow: 

      - /var/log/restjavad.0.log

.. toctree::
   :maxdepth: 1
   :glob:

   lab*