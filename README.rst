libMariaS3
==========

.. image:: https://readthedocs.org/projects/libmarias3/badge/?version=latest
   :target: https://libmarias3.readthedocs.io/en/latest/?badge=latest
   :alt: Documentation Status

This is a lightweight C library to read/write to AWS S3 buckets using objects in memory.

You will need an access key which for AWS can be created at `the AWS security crenditials page <https://console.aws.amazon.com/iam/home?#/security_credentials>`_.

Compiling
---------

.. code-block:: bash

   autoreconf -fi
   ./configure
   make

Testing
-------

libMariaS3 comes with a basic test suite which we recommend executing, especially if you are building for a new platform.

You will need the following OS environment variables set to run the tests:

+------------+----------------------------------------------------------+
| Variable   | Desription                                               |
+============+==========================================================+
| S3KEY      | Your AWS access key                                      |
+------------+----------------------------------------------------------+
| S3SECRET   | Your AWS secret key                                      |
+------------+----------------------------------------------------------+
| S3REGION   | The AWS region (for example us-east-1)                   |
+------------+----------------------------------------------------------+
| S3BUCKET   | The S3 bucket name                                       |
+------------+----------------------------------------------------------+
| S3HOST     | OPTIONAL hostname for non-AWS S3 service                 |
+------------+----------------------------------------------------------+
| S3NOVERIFY | Set to ``1`` if the host should not use SSL verification |
+------------+----------------------------------------------------------+

The test suite is automatically built along with the library and can be executed with ``make check`` or ``make distcheck``.

Credits
-------

The libMariaS3 authors are:

* `Andrew (LinuxJedi) Hutchings <mailto:linuxjedi@mariadb.com>`_
* `Sergei Golubchik <mailto:sergei@mariadb.com>`_
* `Markus Mäkelä <markus.makela@mariadb.com>`_

libMariaS3 uses the following Open Source projects:

* `libcurl <https://curl.haxx.se/>`_
* `libxml2 <http://www.xmlsoft.org/>`_
* `DDM4 <https://github.com/TangentOrg/ddm4>`_
* `Jouni Malinen's SHA256 hash code <j@w1.fi>`_
