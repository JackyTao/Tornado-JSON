Changelog
=========

_
---------

v0.14 - Bugfixes thanks to 100% coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Fixes related to error-writing in ``io_schema`` and ``APIHandler.write_error``


v0.13 - Add asynchronous compatibility to io_schema
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Add asynchronous functionality to io_schema


v0.12 - Python3 support
~~~~~~~~~~~~~~~~~~~~~~~

* Python3.3, in addition to Python2.7, is now supported.


v0.11 - Duplicate route bugfix
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Fixed bug where duplicate routes would be created on existence of multiple HTTP methods.


v0.10 - Route generation with URL patterns
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Route generation will now inspect method signatures in ``APIHandler`` and ``ViewHandler`` subclasses, and construct routes with URL patterns based on the signatures. URL patterns match ``[a-zA-Z0-9_]+``.

**Backwards Compatibility**: ``body`` is no longer provided by ``io_schema`` as the sole argument to HTTP methods. Any existing code using ``body`` can now use ``self.body`` to get the same object.


v0.08 - Input and output example fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Add input_example and output_example fields
* status_code 400 on ValidationError
* Exclude delete from input validation
