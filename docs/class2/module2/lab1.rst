.. |labmodule| replace:: 2
.. |labnum| replace:: 1
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum| – Kibana Interface & Search
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This module will be more instructor lead and investigative. This lab will look at the look and feel of the Kibana interface, and some key navigation hints and tips.

Task 1 - Kibana Interface Explantion
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This task will focus on explation of the Kibana interface and navigating different aspects of the interface.

|interface1|

.. |interface1| image:: /_static/interface1.png
   :width: 12.0in
   :height: 10.0in


Try changing the following:

- Time Range
- Index
- Dashboards

.. NOTE::
	
	Take your time to explore each of the interface elements.


Task 2 - Searching Kibana
^^^^^^^^^^^^^^^^^^^^^^^^^

In this task we will use two example search types to see how Kibana uses elasticsearch. These example searches will be the following:

- Field Search
- Query Bar


**Field Search**
Field searching is very useful in Kibana and can be used to see types of data and values that elasticsearch is indexing. To conduct field searching conduct the following:

	#. Click on a field
	#. Examine the expanded field, note the values that elasticsearch is indexing


|search1|

.. |search1| image:: /_static/search1.png
   :width: 12.0in
   :height: 10.0in


	#. Click the add button.
	#. Notice the field is in the Selected Field section.


|search2|

.. |search2| image:: /_static/search2.png
   :width: 12.0in
   :height: 10.0in


.. NOTE::

	Take time to explore multiple field add to Selected field and build up a set of interesting columns.


**Query Bar**
This type if searching is searching all data fields not only Selected fields as we did previously.

|search3|

.. |search3| image:: /_static/search3.png
   :width: 12.0in
   :height: 10.0in


.. NOTE::

	Take time to explore multiple field add to Selected field and use Query terms to see the results.