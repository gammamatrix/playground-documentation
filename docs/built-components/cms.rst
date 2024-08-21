CMS Packages
############

The Playground CMS provides a content management system, with pages and
snippets, that may be consumed by a Laravel application or served as JSON from a Laravel based API or Resource.

Features:

* Pages and Snippets support revisions.
* Start, Embargo, End and Planned dates are available for controlling content releases.
* Supports custom authorization for each page and snippet: Owner, Groups, po, pg, pw, only_admin, only_user, only_guest, allow_public
* Multiple page types to support magazines, books, articles and more.

.. contents:: Table of Contents


playground-cms
**************

Provides the models for playground-cms-api and playground-cms-resource.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms/develop/resources/docs/artisan-about-playground-cms.png
   :align: center

   ``artisan about`` for playground-cms

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms
    Source on GitHub
        https://github.com/gammamatrix/playground-cms


.. _playground-cms Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\ServiceProvider" --tag playground-config


.. _playground-cms Environment Variables:

Environment Variables
=====================

.. _playground-cms Migrations:

Migrations
----------

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-cms/tree/develop/database/migrations>`_
- NOTE: There are four tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_CMS_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_CMS_LOAD_MIGRATIONS``
    Config: ``playground-cms.load.migrations``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\ServiceProvider" --tag playground-migrations

.. _playground-cms Installation:

Installation
============

NOTE: This package is required by playground-cms-api and playground-cms-resource.

.. code-block:: bash

    composer require gammamatrix/playground-cms


playground-cms-api
******************

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/apis/docs/artisan-about-playground-cms-api.png
..    :align: center

..    ``artisan about`` for playground-cms-api

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-cms-api/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-cms-api/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms-api
    Source on GitHub
        https://github.com/gammamatrix/playground-cms-api

.. _playground-cms-api API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-cms-api/swagger.json <https://github.com/gammamatrix/playground-cms-api/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-cms-api/blob/develop/swagger.json
    Swagger Editor UI
        - https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/swagger.json

.. _playground-cms-api Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\Api\ServiceProvider" --tag="playground-config"

.. _playground-cms-api Environment Variables:

Environment Variables
=====================

.. _playground-cms-api Authentication and Authorization:

Authentication and Authorization
--------------------------------

``PLAYGROUND_CMS_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-cms-api.middleware.default``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_CMS_API_MIDDLEWARE_USER``
    Config: ``playground-cms-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_CMS_API_MIDDLEWARE_GUEST``
    Config: ``playground-cms-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web', EnsureFrontendRequestsAreStateful]``

.. _playground-cms-api Loading:

Loading
-------

``PLAYGROUND_CMS_API_LOAD_POLICIES``
    Config: ``playground-cms-api.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_LOAD_ROUTES``
    Config: ``playground-cms-api.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_LOAD_TRANSLATIONS``
    Config: ``playground-cms-api.load.translations``

    Type: ``bool``

    Default: ``true``

.. _playground-cms-api Revision:

Revision
--------

``PLAYGROUND_CMS_API_ROUTES_OPTIONAL``
    Config: ``playground-cms-api.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_REVISIONS_PAGES``
    Config: ``playground-cms-api.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_REVISIONS_SNIPPETS``
    Config: ``playground-cms-api.revisions.snippets``

    Type: ``bool``

    Default: ``true``


.. _playground-cms-api Routes:

Routes
------

``PLAYGROUND_CMS_API_ROUTES_CMS``
    Config: ``playground-cms-api.routes.cms``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_ROUTES_SNIPPETS``
    Config: ``playground-cms-api.routes.snippets``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_ROUTES_PAGES``
    Config: ``playground-cms-api.routes.pages``

    Type: ``bool``

    Default: ``true``

.. _playground-cms-api Installation:

Installation
============

NOTE: This package requires playground-cms.

.. code-block:: bash

    composer require gammamatrix/playground-cms-api


playground-cms-resource
***********************

Provides an API and a Laravel Blade UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/resources/docs/artisan-about-playground-cms-resource.png
..    :align: center

..    ``artisan about`` for playground-cms-resource

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-cms-resource/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-cms-resource/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-cms-resource

.. _playground-cms-resource API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-cms-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-cms-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-cms-resource/blob/develop/swagger.json
    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/swagger.json

.. _playground-cms-resource Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\Resource\ServiceProvider" --tag playground-config

.. _playground-cms-resource Environment Variables:

Environment Variables
=====================

.. _playground-cms-resource About:

About
-------

``PLAYGROUND_CMS_RESOURCE_ABOUT``
    Config: ``playground-cms-resource.about``

    Type: ``bool``

    Default: ``true``

    Description: Displays information with the `artisan about` command.

.. _playground-cms-resource Authentication and Authorization:

Authentication and Authorization
--------------------------------

If you do not want to use the flexible policies available in Playground, you may publish the config and/or routes to your base application and customize them and the middleware.

The mapping for models to policies is set in `config/playground-cms-resource.php <https://github.com/gammamatrix/playground-cms-resource/blob/develop/config/playground-cms-resource.php>`_ (may also be published).

If you wish to use your own policies, copy from `src/Policies <https://github.com/gammamatrix/playground-cms-resource/tree/develop/src/Policies>`_.


``PLAYGROUND_CMS_RESOURCE_MIDDLEWARE_DEFAULT``
    Config: ``playground-cms-resource.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_CMS_RESOURCE_MIDDLEWARE_USER``
    Config: ``playground-cms-resource.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_CMS_RESOURCE_MIDDLEWARE_GUEST``
    Config: ``playground-cms-resource.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``

.. _playground-cms-resource Loading:

Loading
-------

``PLAYGROUND_CMS_RESOURCE_LOAD_POLICIES``
    Config: ``playground-cms-resource.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_LOAD_ROUTES``
    Config: ``playground-cms-resource.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_LOAD_TRANSLATIONS``
    Config: ``playground-cms-resource.load.translations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_LOAD_VIEWS``
    Config: ``playground-cms-resource.load.views``

    Type: ``bool``

    Default: ``true``

.. _playground-cms-resource Revision:

Revision
--------

``PLAYGROUND_CMS_RESOURCE_ROUTES_OPTIONAL``
    Config: ``playground-cms-resource.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_REVISIONS_PAGES``
    Config: ``playground-cms-resource.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_REVISIONS_SNIPPETS``
    Config: ``playground-cms-resource.revisions.snippets``

    Type: ``bool``

    Default: ``true``

.. _playground-cms-resource Routes:

Routes
------

``PLAYGROUND_CMS_RESOURCE_ROUTES_CMS``
    Config: ``playground-cms-resource.routes.cms``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_ROUTES_PAGES``
    Config: ``playground-cms-resource.routes.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_ROUTES_SNIPPETS``
    Config: ``playground-cms-resource.routes.snippets``

    Type: ``bool``

    Default: ``true``

.. _playground-cms-resource Sitemap:

Sitemap
-------

``PLAYGROUND_CMS_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-cms-resource.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-cms-resource.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_USER``
    Config: ``playground-cms-resource.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-cms-resource.sitemap.view``

    Type: ``string``

    Default: ``playground-cms-resource::sitemap``

    Description: This blade file will be included on the application sitemap.

.. _playground-cms-resource UI:

UI
----

``PLAYGROUND_CMS_RESOURCE_BLADE``
    Config: ``playground-cms-resource.blade``

    Type: ``string``

    Default: ``playground-cms-resource::``

    Description: Sets the view namespace for the package.

.. _playground-cms-resource Installation:

Installation
============

NOTE: This package requires playground-cms.

.. code-block:: bash

    composer require gammamatrix/playground-cms-resource



site-playground-cms-angular
***************************

.. Note::

    - This :term:`CSR` Angular 16 application uses Angular Material and will eventually be generated by `playground-make-angular <https://github.com/gammamatrix/playground-make-angular>`_.
    - https://github.com/gammamatrix/site-playground-cms-angular
