.. role:: kill
   :class: strike

.. role:: kfrag
   :class: strike fragment

.. role:: frag
   :class: fragment

Delivery Pipeline
=================


Teasers
=======

.. class:: pseudocloud

    * :frag:`Containers`
    * :frag:`Gitlab`
    * :kfrag:`Docker`
    * :frag:`Clouds`
    * :frag:`Orchestration`
    * :frag:`Bare-Metal`
    * :frag:`People!`


Background
==========


Early 2014
==========

* 3 Ops
* 3 Dev. Teams
* 1x5 monolith
* 2 Data Centers


Late 2016
=========

* 6 Ops
* 12+7 Dev. Teams
* +6 projects
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


More Features
=============

* Nice commands
* Image rebuild
* Multiple processes
* Image cleanup


Automating Dev. Envs
======================


... that didn't work
====================

* :frag:`1 project`
* :frag:`already set up`
* :frag:`needs learning`
* :frag:`different hosts`


... until we automated deployment
=================================


Idea → Staging
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

* Add tests
* Add metrics
* Add docs
* Add services


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
    * :frag:`—  It's so long` :frag:`(20-30 LoCs)`
    * :frag:`—  Where to copy?`
    * :frag:`—  We have docs? Wow!`


Configs
=======

* containers setup (vagga.yaml)
* 4 × application config
* 3 × container runtime (lithos)
* 3 × deployment config
* gitlab-ci.yaml


Not There
=========

* Network
* Databases
* Replication
* Backups
* Choosing servers


Config
======

* Environment
* Command-line
* Resource constraints


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


That's it
=========

* 31 services in 5 months
* 12 Doc projects
* 148 Gitlab Repos


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

