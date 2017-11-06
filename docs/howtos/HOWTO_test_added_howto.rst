HOWTO - how to do stuff
------------------------------------------------------------------

Twill put extra stuff into here

Task 1 – Update unknown index fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

At times new fields may appear in the index field based on software version or addiitonal logging from irules. It will be requried to update the index to make these fields usable.

|howto1|

.. |howto1| image:: /_static/howto1.png
   :width: 12.0in
   :height: 6.0in

.. NOTE::
  Notice the ? symbol next to the field.


Update by clicking on the refresh button

|howto2|

.. |howto2| image:: /_static/howto2.png
   :width: 6.0in
   :height: 3.0in


**Note the increased change**

|howto3|

.. |howto3| image:: /_static/howto3.png
   :width: 2.0in
   :height: 1.0in



Task 2 - Manual Index Changes 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Index changes in json can be done manually if importing from another system.

#. Create a new search or visualisation
#. Export the new search json
#. Open the json and copy the index id
#. Open the json to be imported and paste the updated index id
