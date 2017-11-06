.. |labmodule| replace:: 1
.. |labnum| replace:: 1
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Install the Ubuntu Base
-----------------------------------------------------

In this lab you will walk through installing the ubuntu
base ready for ELK stack

Task 1 - Install additional software required for ELK Stack
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::
	
	sudo apt-get install software-properties-common
	sudo apt install curl


Task 2 - Add and install Java
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

	sudo add-apt-repository -y ppa:webupd8team/java
	sudo apt-get update
	sudo apt-get -y install oracle-java8-installer