CRM Packages
============

The Playground CRM provides a content management system, with pages and
snippets, that may be consumed by a Laravel application or served as JSON from a Laravel based API or Resource.

Features:

* Pages and Snippets support revisions.
* Start, Embargo, End and Planned dates are available for controlling content releases.
* Supports custom authorization for each page and snippet: Owner, Groups, po, pg, pw, only_admin, only_user, only_guest, allow_public
* Multiple page types to support magazines, books, articles and more.

.. contents:: Table of Contents


playground-crm
--------------

Provides the models for playground-crm-api and playground-crm-resource.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm/develop/resources/docs/artisan-about-playground-crm.png
..    :align: center

..    ``artisan about`` for playground-crm

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-crm
    Source on GitHub
        https://github.com/gammamatrix/playground-crm


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\ServiceProvider" --tag="playground-config"


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Migrations
""""""""""

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-crm/tree/develop/database/migrations>`_
- NOTE: There are 15 tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_CRM_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_CRM_LOAD_MIGRATIONS``
    Config: ``playground-crm-resource.middleware.default``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\ServiceProvider" --tag="playground-migrations"

Installation
^^^^^^^^^^^^

NOTE: This package is required by playground-crm-api and playground-crm-resource.

.. code-block:: bash

    composer require gammamatrix/playground-crm


playground-crm-api
------------------

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/apis/docs/artisan-about-playground-crm-api.png
..    :align: center

..    ``artisan about`` for playground-crm-api

.. admonition:: Package Information

    Packagist
        packagist.org/packages/gammamatrix/playground-crm-api
    Source on GitHub
        https://github.com/gammamatrix/playground-crm-api


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the gammamatrix/playground-crm-api/swagger.json provided in the repository packagist.org/packages/gammamatrix/playground-crm-api/swagger.json.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/swagger.json
    Redocly
        redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-api/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\Api\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

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


Loading
"""""""

``PLAYGROUND_CRM_API_LOAD_POLICIES``
    Config: ``playground-crm-api.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_LOAD_ROUTES``
    Config: ``playground-crm-api.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_LOAD_TRANSLATIONS``
    Config: ``playground-crm-api.middleware.load.translations``

    Type: ``bool``

    Default: ``true``


Revision
""""""""

``PLAYGROUND_CRM_API_ROUTES_OPTIONAL``
    Config: ``playground-crm-api.middleware.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_REVISIONS_PAGES``
    Config: ``playground-crm-api.middleware.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_REVISIONS_SNIPPETS``
    Config: ``playground-crm-api.middleware.revisions.snippets``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_CRM_API_ROUTES_CRM``
    Config: ``playground-crm-api.routes.crm``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_SNIPPETS``
    Config: ``playground-crm-api.routes.snippets``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_API_ROUTES_PAGES``
    Config: ``playground-crm-api.routes.pages``

    Type: ``bool``

    Default: ``true``

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-crm.

.. code-block:: bash

    composer require gammamatrix/playground-crm-api


playground-crm-resource
-----------------------

Provides an API and a Laravel Blade UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/resources/docs/artisan-about-playground-crm-resource.png
..    :align: center

..    ``artisan about`` for playground-crm-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-crm-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-crm-resource


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-crm-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-crm-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-crm-resource/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Crm\Resource\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

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


Loading
"""""""

``PLAYGROUND_CRM_RESOURCE_LOAD_POLICIES``
    Config: ``playground-crm-resource.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_LOAD_ROUTES``
    Config: ``playground-crm-resource.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_LOAD_VIEWS``
    Config: ``playground-crm-resource.middleware.load.views``

    Type: ``bool``

    Default: ``true``


Revision
""""""""

``PLAYGROUND_CRM_RESOURCE_ROUTES_OPTIONAL``
    Config: ``playground-crm-resource.middleware.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_REVISIONS_PAGES``
    Config: ``playground-crm-resource.middleware.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_REVISIONS_SNIPPETS``
    Config: ``playground-crm-resource.middleware.revisions.snippets``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_CRM_RESOURCE_ROUTES_CRM``
    Config: ``playground-crm-resource.routes.crm``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_PAGES``
    Config: ``playground-crm-resource.routes.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_ROUTES_SNIPPETS``
    Config: ``playground-crm-resource.routes.snippets``

    Type: ``bool``

    Default: ``true``


Sitemap
"""""""

``PLAYGROUND_CRM_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-crm-resource.middleware.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-crm-resource.middleware.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_USER``
    Config: ``playground-crm-resource.middleware.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CRM_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-crm-resource.middleware.sitemap.view``

    Type: ``string``

    Default: ``playground-crm-resource::sitemap``

    Description: This blade file will be included on the application sitemap.


UI
""

``PLAYGROUND_CRM_RESOURCE_BLADE``
    Config: ``playground-crm-resource.blade``

    Type: ``string``

    Default: ``playground-crm-resource::``

    Description: Sets the view namespace for the package.

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-crm.

.. code-block:: bash

    composer require gammamatrix/playground-crm-resource
