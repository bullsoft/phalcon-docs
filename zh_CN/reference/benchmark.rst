框架基准程序
====================

之前性能并不是 WEB 开发首要关注的问题，因为合理的硬件能弥补代码性能。但是自从 Google 决定_把站点打开速度加入搜索排序算法中后，性能和功能一样成为 WEB 开发需要关注的重点。也就是说，通过提升网站性能也能够给网站带来正面影响。

In the past, performance was not considered one of the top priorities when developing web applications. Reasonable hardware was able to compensate for that. However when Google decided_ to take site speed into account in the search rankings, performance became one of the top priorities alongside functionality. This is yet another way in which improving web performance will have a positive impact on a website.

下面的基准测试程序，会体现 Phalcon 跟传统 PHP 框架相比的性能优势。这些基准测试程序都已经更新到相应框架的最新正式版，Phalcon 也不例外。

The benchmarks below, show how efficient Phalcon is when compared with other traditional PHP frameworks. These benchmarks are updated as stable versions are released from any of the frameworks mentioned or Phalcon itself.

我们鼓励开发者克隆我们基准程序使用的测试用例代码。如果你有任何其他优化手段或建议，请不吝'告诉我们_'。'从 Github 检出代码'_

We encourage programmers to clone the test suite that we are using for our benchmarks. If you have any additional optimizations or comments please `write us`_. `Check out source at Github`_

测试环境
------------------------------

测试过程中为所有框架都打开了 APC_ OPCODE 缓存。出于性能考虑，所有的 Apache 的 mod-rewrite 特性都被禁用了。

APC_ intermediate code cache was enabled for all frameworks. Any Apache mod-rewrite feature was disabled when possible to avoid potentially additional overheads.

测试硬件环境如下：

The testing hardware environment is as follows:

* Operating System: Mac OS X Lion 10.7.4
* Web Server: Apache httpd 2.2.22
* PHP: 5.3.15
* CPU: 2.04 Ghz Intel Core i5
* Main Memory: 4GB 1333 MHz DDR3
* Hard Drive: 500GB SATA Disk

*PHP 版本和信息：*

*PHP version and info:*

.. figure:: ../_static/img/bench-4.png
    :align: center

*APC settings:*

.. figure:: ../_static/img/bench-5.png
    :align: center


基准程序列表：
-----------------------

.. toctree::
   :maxdepth: 1

   benchmark/hello-world
   benchmark/micro

更新日志
---------

.. versionadded:: 1.0
    Update Mar-20-2012: Benchmarks redone changing the apc.stat setting to Off. More Info

.. versionchanged:: 1.1
    Update May-13-2012: Benchmarks redone PHP plain templating engine instead of Twig for Symfony. Configuration settings for Yii were also changed as recommended.

.. versionchanged:: 1.2
    Update May-20-2012: Fuel framework was added to benchmarks.

.. versionchanged:: 1.3
    Update Jun-4-2012: Cake framework was added to benchmarks. It is not however present in the graphics, since it takes  30 seconds to run only 10 of 1000.

.. versionchanged:: 1.4
    Update Ago-27-2012: PHP updated to 5.3.15, APC updated to 3.1.11, Yii updated to 1.1.12, Phalcon updated to 0.5.0, Added Laravel, OS updated to Mac OS X Lion. Hardware upgraded.

   benchmark/hello-world

.. _decided: http://googlewebmastercentral.blogspot.com/2010/04/using-site-speed-in-web-search-ranking.html
.. _write us: http://phalcon.uservoice.com/
.. _Check out source at Github: https://github.com/phalcon/framework-bench
.. _APC: http://php.net/manual/en/book.apc.php

