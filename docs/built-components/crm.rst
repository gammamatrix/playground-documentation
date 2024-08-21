CRM Packages
############

The Playground CRM provides a client relations management system, with clients, contacts, locations, organizations, and people, that may be utlized by a Laravel application or served as JSON from a Laravel based API or Resource.

Features:

* Provides models for clients, contacts, organizations and people.

.. contents:: Table of Contents


playground-crm
**************

Provides the models for playground-crm-api and playground-crm-resource.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm/develop/resources/docs/artisan-about-playground-crm.png
..    :align: center

..    ``artisan about`` for playground-crm

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-crm
    Source on GitHub
        https://github.com/gammamatrix/playground-crm


.. _playground-crm Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\ServiceProvider" --tag playground-config


.. _playground-crm Environment Variables:

Environment Variables
=====================

.. _playground-crm Migrations:

Migrations
----------

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-crm/tree/develop/database/migrations>`_
- NOTE: There are four tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_CRM_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_CRM_LOAD_MIGRATIONS``
    Config: ``playground-crm.load.migrations``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\ServiceProvider" --tag playground-migrations

.. _playground-crm Installation:

Installation
============

NOTE: This package is required by playground-crm-api and playground-crm-resource.

.. code-block:: bash

    composer require gammamatrix/playground-crm


playground-crm-api
******************

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/apis/docs/artisan-about-playground-crm-api.png
..    :align: center

..    ``artisan about`` for playground-crm-api

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-crm-api/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-crm-api/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-crm-api
    Source on GitHub
        https://github.com/gammamatrix/playground-crm-api

.. _playground-crm-api API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-crm-api/swagger.json <https://github.com/gammamatrix/playground-crm-api/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-crm-api/blob/develop/swagger.json
    Swagger Editor UI
        - https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/swagger.json

.. _playground-crm-api Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\Api\ServiceProvider" --tag="playground-config"

.. _playground-crm-api Environment Variables:

Environment Variables
=====================

.. _playground-crm-api Authentication and Authorization:

Authentication and Authorization
--------------------------------

``PLAYGROUND_CRM_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-crm-api.middleware.default``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_CRM_API_MIDDLEWARE_USER``
    Config: ``playground-crm-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_CRM_API_MIDDLEWARE_GUEST``
    Config: ``playground-crm-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web', EnsureFrontendRequestsAreStateful]``

.. _playground-crm-api Loading:

Loading
-------

``PLAYGROUND_CRM_API_LOAD_POLICIES``
    Config: ``playground-crm-api.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_LOAD_ROUTES``
    Config: ``playground-crm-api.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_LOAD_TRANSLATIONS``
    Config: ``playground-crm-api.load.translations``

    Type: ``bool``

    Default: ``true``

.. _playground-crm-api Routes:

Routes
------

``PLAYGROUND_CRM_API_ROUTES_CRM``
    Config: ``playground-crm-api.routes.crm``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_CLIENTS``
    Config: ``playground-crm-api.routes.clients``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_CONTACTS``
    Config: ``playground-crm-api.routes.contacts``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_LOCATIONS``
    Config: ``playground-crm-api.routes.locations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_ORGANIZATIONS``
    Config: ``playground-crm-api.routes.organizations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_PEOPLES``
    Config: ``playground-crm-api.routes.peoples``

    Type: ``bool``

    Default: ``true``

.. _playground-crm-api Installation:

Installation
============

NOTE: This package requires playground-crm.

.. code-block:: bash

    composer require gammamatrix/playground-crm-api


playground-crm-resource
***********************

Provides an API and a Laravel Blade UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/resources/docs/artisan-about-playground-crm-resource.png
..    :align: center

..    ``artisan about`` for playground-crm-resource

.. admonition:: Package Information

    Continuous Integration with GitHub Actions
        https://github.com/gammamatrix/playground-crm-resource/actions
    GitHub Actions Workflow
        https://github.com/gammamatrix/playground-crm-resource/blob/develop/.github/workflows/ci.yml
    Packagist
        https://packagist.org/packages/gammamatrix/playground-crm-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-crm-resource

.. _playground-crm-resource API Documentation:

API Documentation
=================

Documentation is generated from the `gammamatrix/playground-crm-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-crm-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    OpenAPI Documentation Configuration
        - https://github.com/gammamatrix/playground-crm-resource/blob/develop/swagger.json
    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/swagger.json

.. _playground-crm-resource Configuration:

Configuration
=============

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\Resource\ServiceProvider" --tag playground-config

.. _playground-crm-resource Environment Variables:

Environment Variables
=====================

.. _playground-crm-resource About:

About
-------

``PLAYGROUND_CRM_RESOURCE_ABOUT``
    Config: ``playground-crm-resource.about``

    Type: ``bool``

    Default: ``true``

    Description: Displays information with the `artisan about` command.

.. _playground-crm-resource Authentication and Authorization:

Authentication and Authorization
--------------------------------

If you do not want to use the flexible policies available in Playground, you may publish the config and/or routes to your base application and customize them and the middleware.

The mapping for models to policies is set in `config/playground-crm-resource.php <https://github.com/gammamatrix/playground-crm-resource/blob/develop/config/playground-crm-resource.php>`_ (may also be published).

If you wish to use your own policies, copy from `src/Policies <https://github.com/gammamatrix/playground-crm-resource/tree/develop/src/Policies>`_.


``PLAYGROUND_CRM_RESOURCE_MIDDLEWARE_DEFAULT``
    Config: ``playground-crm-resource.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_CRM_RESOURCE_MIDDLEWARE_USER``
    Config: ``playground-crm-resource.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_CRM_RESOURCE_MIDDLEWARE_GUEST``
    Config: ``playground-crm-resource.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``

.. _playground-crm-resource Loading:

Loading
-------

``PLAYGROUND_CRM_RESOURCE_LOAD_POLICIES``
    Config: ``playground-crm-resource.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_LOAD_ROUTES``
    Config: ``playground-crm-resource.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_LOAD_TRANSLATIONS``
    Config: ``playground-crm-resource.load.translations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_LOAD_VIEWS``
    Config: ``playground-crm-resource.load.views``

    Type: ``bool``

    Default: ``true``

.. _playground-crm-resource Routes:

Routes
------

``PLAYGROUND_CRM_RESOURCE_ROUTES_CRM``
    Config: ``playground-crm-resource.routes.crm``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_CLIENTS``
    Config: ``playground-crm-resource.routes.clients``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_CONTACTS``
    Config: ``playground-crm-resource.routes.contacts``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_LOCATIONS``
    Config: ``playground-crm-resource.routes.locations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_ORGANIZATIONS``
    Config: ``playground-crm-resource.routes.organizations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_PEOPLES``
    Config: ``playground-crm-resource.routes.peoples``

    Type: ``bool``

    Default: ``true``

.. _playground-crm-resource Sitemap:

Sitemap
-------

``PLAYGROUND_CRM_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-crm-resource.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-crm-resource.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_USER``
    Config: ``playground-crm-resource.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-crm-resource.sitemap.view``

    Type: ``string``

    Default: ``playground-crm-resource::sitemap``

    Description: This blade file will be included on the application sitemap.

.. _playground-crm-resource UI:

UI
----

``PLAYGROUND_CRM_RESOURCE_BLADE``
    Config: ``playground-crm-resource.blade``

    Type: ``string``

    Default: ``playground-crm-resource::``

    Description: Sets the view namespace for the package.

.. _playground-crm-resource Installation:

Installation
============

NOTE: This package requires playground-crm.

.. code-block:: bash

    composer require gammamatrix/playground-crm-resource



site-playground-crm-angular
***************************

.. Note::

    - This :term:`CSR` Angular application uses Angular Material and will eventually be generated by `playground-make-angular <https://github.com/gammamatrix/playground-make-angular>`_.
