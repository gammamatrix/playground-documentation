Directory Packages
##################

The Playground Directory provides a directory management system, with locations and sublocations, that may be consumed by a Laravel application or served as JSON from a Laravel based API or Resource.

Features:

* Locations and Sublocations support revisions.
* Start, Embargo, End and Planned dates are available for controlling directory releases.
* Supports custom authorization for each location and sublocation: Owner, Groups, po, pg, pw, only_admin, only_user, only_guest, allow_public

.. contents:: Table of Contents


playground-directory
********************

Provides the models for playground-directory-api and playground-directory-resource.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-directory/develop/resources/docs/artisan-about-playground-directory.png
..    :align: center

..    ``artisan about`` for playground-directory

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-directory
    Source on GitHub
        https://github.com/gammamatrix/playground-directory


.. _playground-directory Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Directory\ServiceProvider" --tag playground-config


.. _playground-directory Environment Variables:

Environment Variables
=====================

.. _playground-directory Migrations:

Migrations
----------

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-directory/tree/develop/database/migrations>`_
- NOTE: There are four tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_DIRECTORY_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_DIRECTORY_LOAD_MIGRATIONS``
    Config: ``playground-directory.load.migrations``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Directory\ServiceProvider" --tag playground-migrations

.. _playground-directory Installation:

Installation
============

NOTE: This package is required by playground-directory-api and playground-directory-resource.

.. code-block:: bash

    composer require gammamatrix/playground-directory


playground-directory-api
************************

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-directory-api/develop/apis/docs/artisan-about-playground-directory-api.png
..    :align: center

..    ``artisan about`` for playground-directory-api

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-directory-api/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-directory-api/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-directory-api
    Source on GitHub
        https://github.com/gammamatrix/playground-directory-api

.. _playground-directory-api API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-directory-api/swagger.json <https://github.com/gammamatrix/playground-directory-api/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-directory-api/blob/develop/swagger.json
    Swagger Editor UI
        - https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-directory-api/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-directory-api/develop/swagger.json

.. _playground-directory-api Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Directory\Api\ServiceProvider" --tag="playground-config"

.. _playground-directory-api Environment Variables:

Environment Variables
=====================

.. _playground-directory-api Authentication and Authorization:

Authentication and Authorization
--------------------------------

``PLAYGROUND_DIRECTORY_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-directory-api.middleware.default``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_DIRECTORY_API_MIDDLEWARE_USER``
    Config: ``playground-directory-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_DIRECTORY_API_MIDDLEWARE_GUEST``
    Config: ``playground-directory-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web', EnsureFrontendRequestsAreStateful]``

.. _playground-directory-api Loading:

Loading
-------

``PLAYGROUND_DIRECTORY_API_LOAD_POLICIES``
    Config: ``playground-directory-api.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_LOAD_ROUTES``
    Config: ``playground-directory-api.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_LOAD_TRANSLATIONS``
    Config: ``playground-directory-api.load.translations``

    Type: ``bool``

    Default: ``true``

.. _playground-directory-api Revision:

Revision
--------

``PLAYGROUND_DIRECTORY_API_ROUTES_OPTIONAL``
    Config: ``playground-directory-api.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_REVISIONS_LOCATIONS``
    Config: ``playground-directory-api.revisions.locations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_REVISIONS_SUBLOCATIONS``
    Config: ``playground-directory-api.revisions.sublocations``

    Type: ``bool``

    Default: ``true``


.. _playground-directory-api Routes:

Routes
------

``PLAYGROUND_DIRECTORY_API_ROUTES_DIRECTORY``
    Config: ``playground-directory-api.routes.directory``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_ROUTES_SUBLOCATIONS``
    Config: ``playground-directory-api.routes.sublocations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_API_ROUTES_LOCATIONS``
    Config: ``playground-directory-api.routes.locations``

    Type: ``bool``

    Default: ``true``

.. _playground-directory-api Installation:

Installation
============

NOTE: This package requires playground-directory.

.. code-block:: bash

    composer require gammamatrix/playground-directory-api


playground-directory-resource
*****************************

Provides an API and a Laravel Blade UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-directory-resource/develop/resources/docs/artisan-about-playground-directory-resource.png
..    :align: center

..    ``artisan about`` for playground-directory-resource

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-directory-resource/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-directory-resource/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-directory-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-directory-resource

.. _playground-directory-resource API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-directory-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-directory-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-directory-resource/blob/develop/swagger.json
    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-directory-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-directory-resource/develop/swagger.json

.. _playground-directory-resource Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Directory\Resource\ServiceProvider" --tag playground-config

.. _playground-directory-resource Environment Variables:

Environment Variables
=====================

.. _playground-directory-resource About:

About
-------

``PLAYGROUND_DIRECTORY_RESOURCE_ABOUT``
    Config: ``playground-directory-resource.about``

    Type: ``bool``

    Default: ``true``

    Description: Displays information with the `artisan about` command.

.. _playground-directory-resource Authentication and Authorization:

Authentication and Authorization
--------------------------------

If you do not want to use the flexible policies available in Playground, you may publish the config and/or routes to your base application and customize them and the middleware.

The mapping for models to policies is set in `config/playground-directory-resource.php <https://github.com/gammamatrix/playground-directory-resource/blob/develop/config/playground-directory-resource.php>`_ (may also be published).

If you wish to use your own policies, copy from `src/Policies <https://github.com/gammamatrix/playground-directory-resource/tree/develop/src/Policies>`_.


``PLAYGROUND_DIRECTORY_RESOURCE_MIDDLEWARE_DEFAULT``
    Config: ``playground-directory-resource.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_DIRECTORY_RESOURCE_MIDDLEWARE_USER``
    Config: ``playground-directory-resource.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_DIRECTORY_RESOURCE_MIDDLEWARE_GUEST``
    Config: ``playground-directory-resource.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``

.. _playground-directory-resource Loading:

Loading
-------

``PLAYGROUND_DIRECTORY_RESOURCE_LOAD_POLICIES``
    Config: ``playground-directory-resource.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_LOAD_ROUTES``
    Config: ``playground-directory-resource.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_LOAD_TRANSLATIONS``
    Config: ``playground-directory-resource.load.translations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_LOAD_VIEWS``
    Config: ``playground-directory-resource.load.views``

    Type: ``bool``

    Default: ``true``

.. _playground-directory-resource Revision:

Revision
--------

``PLAYGROUND_DIRECTORY_RESOURCE_ROUTES_OPTIONAL``
    Config: ``playground-directory-resource.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_REVISIONS_LOCATIONS``
    Config: ``playground-directory-resource.revisions.locations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_REVISIONS_SUBLOCATIONS``
    Config: ``playground-directory-resource.revisions.sublocations``

    Type: ``bool``

    Default: ``true``

.. _playground-directory-resource Routes:

Routes
------

``PLAYGROUND_DIRECTORY_RESOURCE_ROUTES_DIRECTORY``
    Config: ``playground-directory-resource.routes.directory``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_ROUTES_LOCATIONS``
    Config: ``playground-directory-resource.routes.locations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_ROUTES_SUBLOCATIONS``
    Config: ``playground-directory-resource.routes.sublocations``

    Type: ``bool``

    Default: ``true``

.. _playground-directory-resource Sitemap:

Sitemap
-------

``PLAYGROUND_DIRECTORY_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-directory-resource.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-directory-resource.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_SITEMAP_USER``
    Config: ``playground-directory-resource.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_DIRECTORY_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-directory-resource.sitemap.view``

    Type: ``string``

    Default: ``playground-directory-resource::sitemap``

    Description: This blade file will be included on the application sitemap.

.. _playground-directory-resource UI:

UI
----

``PLAYGROUND_DIRECTORY_RESOURCE_BLADE``
    Config: ``playground-directory-resource.blade``

    Type: ``string``

    Default: ``playground-directory-resource::``

    Description: Sets the view namespace for the package.

.. _playground-directory-resource Installation:

Installation
============

NOTE: This package requires playground-directory.

.. code-block:: bash

    composer require gammamatrix/playground-directory-resource



site-playground-directory-angular
*********************************

.. Note::

    - This :term:`CSR` Angular application uses Angular Material and will eventually be generated by `playground-make-angular <https://github.com/gammamatrix/playground-make-angular>`_.
