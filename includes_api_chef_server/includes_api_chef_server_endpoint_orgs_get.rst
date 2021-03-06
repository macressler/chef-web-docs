.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The ``GET`` method is used to get a list of organizations on the |chef server|.

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/NAME/organizations

**Response**

The response is similar to:

.. code-block:: javascript

   {
     "org_name1"=>"https://url/for/org_name1"
     "org_name2"=>"https://url/for/org_name2"
	 ...
   }

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``403``
     - |response code 403 forbidden|

