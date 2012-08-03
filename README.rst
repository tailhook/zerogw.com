==================
Zerogw.com Website
==================

Zerogw is an HTTP web server. So zerogw website is by zerogw itself.


Dependencies
============

* zerogw
* python3 (tabbedchat example)
* redis-server (tabbedchat example)
* procboss (optional)


Running Locally
===============

In case you want only static serving::

    zerogw -c config/zerogw-local.yaml

In case you want everything running, you'd better run with procboss::

    mkdir run
    bossrun


Production Running
==================

The configuration files are ready for running at localhost. To run production
service do the following modifications

Modify ``routes.yaml``:

* Turn paths to absolute and enable ``restrict-root``
* Set ``$zerogw_com`` to ``zerogw.com``
* set ``$sockets`` directory

Overall:

* Include ``routes.yaml`` to your config
* Include all needed processes into your supervisor's configuration
