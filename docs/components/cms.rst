CMS
===

Playground provides components across packages to handle the needs of an application.

Packages
--------

The Playground CMS provides pages and snippets they may be consumed by a Laravel application or served as JSON from an API or Resource.

Features:

* Pages and Snippets support revisions.
* Start, Embargo, End and Planned dates are available for controlling content releases.
* Supports custom authorization for each page and snippet: Owner, Groups, po, pg, pw, only_admin, only_user, only_guest, allow_public
* Multiple page types to support magazines, books, articles and more.


playground-cms
^^^^^^^^^^^^^^

Provides the models for playground-cms-api and playground-cms-resource.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms/develop/resources/docs/artisan-about-playground-cms.png
   :align: center

   ``artisan about`` for playground-cms


.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms
    Source on GitHub
        https://github.com/gammamatrix/playground-cms



playground-cms-resource
^^^^^^^^^^^^^^^^^^^^^^^

Provides an API and a Laravel Blade UI for managing pages and snippets for content.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cmss-resource/develop/resources/docs/artisan-about-playground-cms-resource.png
..    :align: center

..    ``artisan about`` for playground-cms-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-cms-resource
