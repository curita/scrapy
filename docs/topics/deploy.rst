.. _topics-deploy:

=================
Deploying Spiders
=================

This section describes the different options you have for deploying your Scrapy
spiders to run them on a regular basis. Running Scrapy spiders in your local
machine is very convenient for the (early) development stage, but not so much
when you need to execute long-running spiders or move spiders to run in
production continously. This is where the solutions for deploying Scrapy
spiders come in.

Popular choices for deploying Scrapy spiders are:

* :ref:`Scrapyd <deploy-scrapyd>` (open source)
* :ref:`Scrapy Cloud <deploy-scrapy-cloud>` (cloud-based)

.. _deploy-scrapyd:

Deploying to a Scrapyd Server
=============================

`Scrapyd`_ is an open source application to run Scrapy spiders. It provides
a server with HTTP API, capable of running and monitoring Scrapy spiders.

To deploy spiders to Scrapyd, you can use the scrapyd-deploy tool provided by
the `scrapyd-client`_ package. Please refer to the `scrapyd-deploy
documentation`_ for more information.

Scrapyd is maintained by some of the Scrapy developers.

.. _deploy-scrapy-cloud:

Deploying to Scrapy Cloud
=========================

`Scrapy Cloud`_ is a hosted, cloud-based service by `Scrapinghub`_,
the company behind Scrapy.

Scrapy Cloud removes the need to setup and monitor servers
and provides a nice UI to manage spiders and review scraped items,
logs and stats.

To deploy spiders to Scrapy Cloud you can use the `shub`_ command line tool.
Please refer to the `Scrapy Cloud documentation`_ for more information.

Scrapy Cloud is compatible with Scrapyd and one can switch between
them as needed - the configuration is read from the ``scrapy.cfg`` file
just like ``scrapyd-deploy``.

.. _Scrapyd: https://github.com/scrapy/scrapyd
.. _Deploying your project: https://scrapyd.readthedocs.org/en/latest/deploy.html
.. _Scrapy Cloud: http://scrapinghub.com/scrapy-cloud/
.. _scrapyd-client: https://github.com/scrapy/scrapyd-client
.. _shub: http://doc.scrapinghub.com/shub.html
.. _scrapyd-deploy documentation: http://scrapyd.readthedocs.org/en/latest/deploy.html
.. _Scrapy Cloud documentation: http://doc.scrapinghub.com/scrapy-cloud.html
.. _Scrapinghub: http://scrapinghub.com/
