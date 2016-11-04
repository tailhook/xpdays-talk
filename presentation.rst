.. role:: kill
   :class: strike

.. role:: frag
   :class: fragment

Delivery Pipeline
=================


Teasers
=======

(TODO: should be tag cloud, more things)

* Gitlab
* Containers
* :kill:`Docker`
* Orchestration


Background
==========


Early 2014
==========

* 3 Ops
* 3 Dev. Teams
* 5×5 services
* 2 Data Centers


Late 2016
=========

* 6 Ops
* 5+7 Dev. Teams
* 140 Repos
* +8 services
* 31 new-style
* 6 Data Centers
* ~ 400 servers


Challenges
==========


1. Don't Break
===============


2. No Spare Hardware
=====================

(tight limits)


3. Teaching
============


4. Containers
=======================

Containers ≠ Docker


5. No SPoF
==========


6. Security
===========


(TODO: Some Final slide for Background Section)
===============================================


Implementation
==============


Started with Dev. Envs
======================


Installation
============

.. code-block:: console

    > git clone
    > vagga run


Updating
========

.. code-block:: console

    > git pull
    > vagga run


Instead of
==========

.. code-block:: console

    > pip install ..
    # oh, didn't work
    # ask somebody
    > apt-get install ...
    > pip install ...
    # edit something else
    # repeat
    > npm install ...


Instead of
==========

.. class:: dashlist

    * —  I've found a bug !
    * —  Have you done ``pip install`` ?
    * —  Yes
    * —  ``npm purge; npm install`` ?
    * —  Oh, that did work!


Automating Dev. Envs
======================


... that didn't work
====================


... until we automated deployment
=================================


Idea -> Staging
===============


Create a Repo
=============

Go to gitlab, and press a button


Create Some Tests
=================

* Add ``.gitlab-ci.yml`` to a repo
* Containers with vagga


Deploy to Staging
=================

* Add few configs


Out of the Box
==============

* Clean environment
* Logging
* Metrics


Iterate
=======

* Add metrics

Staging: Updates
================

1. Every commit
2. Tag (stable)


Idea → Staging
===============

* Create a Repo
* Write few configs



Idea → Production
==================

* Create a Repo
* Write few configs
* Ask Ops For Deployment Key
* Write more configs
* :frag:`broken down in ~15 steps`


Updates
=======

* Tag + Push the Button


Challenges
==========

* Teaching
* Security


Challenges: Teaching
====================

.. class:: dashlist

    * :frag:`—  Why should I write config?`
    * :frag:`—  It's so long (20-30 LoCs)`
    * :frag:`—  Where to copy?`
    * :frag:`—  We have docs? Wow!`


Config
======

* Environment
* Command-line
* Resource constraints


Not There
=========

* Network
* Databases
* Replication
* Backups
* Choosing servers


Solution: Patience
==================

.. class:: dashlist

    * :frag:`—  Wow! I'm in charge now?`
    * :frag:`—  Just update it here, right?`
    * :frag:`—  I can deploy it myself?`
    * :frag:`—  Can I break something?`


Security
========

* Containers
* Sandboxing at all layers
* ``+`` Ops


Plans
=====


Benchmarking Cluster
====================

With the same level of easyness


Network Isolation
=================

For each project or even for subprojects


Database Deployment
===================

Basically presets for our commonly used databases and memory-caches, including replication, backup...


Questions
=========

