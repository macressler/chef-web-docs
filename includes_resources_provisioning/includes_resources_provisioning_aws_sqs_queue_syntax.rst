.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


A ``aws_sqs_queue`` resource block manages queues in |amazon sqs|. For example:

.. code-block:: ruby

   aws_sqs_queue 'name' do
     options({ :delay_seconds => 1 })
   end

The full syntax for all of the properties that are available to the ``aws_sqs_queue`` resource is:

.. code-block:: ruby

   aws_sqs_queue 'name' do
     options                       Hash
   end

where 

* ``aws_sqs_queue`` is the resource
* ``name`` is the name of the resource block and also the name of a queue in |amazon sqs|
* ``options`` is a property of this resource, with the |ruby| type shown. |see attributes|
