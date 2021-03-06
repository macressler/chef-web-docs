.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The value of the ``revision`` attribute may change over time. From one branch to another, to a tag, to a specific SHA for a commit, and then back to a branch. The ``revision`` attribute may even be changed in a way where history gets rewritten. 

Instead of tracking a specific branch or doing a headless checkout, the |chef client| maintains its own branch (via the |resource scm_git| resource) that does not exist in the upstream repository. The |chef client| is then free to forcibly check out this branch to any commit without destroying the local history of an existing branch. 

For example, to explicitly track an upstream repository's master branch:

.. code-block:: ruby

   revision 'master'

Use the ``git rev-parse`` and ``git ls-remote`` commands to verify that the |chef client| is synchronizing commits correctly. (The |chef client| always runs ``git ls-remote`` on the upstream repository to verify the commit is made to the correct repository.)
