Lead Packages
===============

The Playground Lead provides a project management system that may be consumed
by a Laravel application or served as JSON from a Laravel based API or Resource.

.. contents:: Table of Contents


playground-lead
-----------------

Provides the models for playground-lead-api and playground-lead-resource.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-lead/develop/resources/docs/artisan-about-playground-lead.png
   :align: center

   ``artisan about`` for playground-lead

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-lead
    Source on GitHub
        https://github.com/gammamatrix/playground-lead


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Lead\ServiceProvider" --tag="playground-config"


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Migrations
""""""""""

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-lead/tree/develop/database/migrations>`_
- NOTE: There are 15 tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_LEAD_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_LEAD_LOAD_MIGRATIONS``
    Config: ``playground-lead-resource.middleware.default``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Lead\ServiceProvider" --tag="playground-migrations"

Installation
^^^^^^^^^^^^

NOTE: This package is required by playground-lead-api and playground-lead-resource.

.. code-block:: bash

    composer require gammamatrix/playground-lead


playground-lead-api
---------------------

Provides an API, without a UI for the Playground Project Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-lead-api/develop/apis/docs/artisan-about-playground-lead-api.png
..    :align: center

..    ``artisan about`` for playground-lead-api

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-lead-api
    Source on GitHub
        https://github.com/gammamatrix/playground-lead-api


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-lead-api/swagger.json provided in the repository <https://github.com/gammamatrix/playground-lead-api/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-lead-api/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-lead-api/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Lead\Api\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

``PLAYGROUND_LEAD_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-lead-api.middleware.default``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_LEAD_API_MIDDLEWARE_USER``
    Config: ``playground-lead-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth:sanctum', EnsureFrontendRequestsAreStateful]``

``PLAYGROUND_LEAD_API_MIDDLEWARE_GUEST``
    Config: ``playground-lead-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web' EnsureFrontendRequestsAreStateful]``


Loading
"""""""

``PLAYGROUND_LEAD_API_LOAD_POLICIES``
    Config: ``playground-lead-api.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_LOAD_ROUTES``
    Config: ``playground-lead-api.middleware.load.routes``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_LEAD_API_ROUTES_CAMPAIGNS``
    Config: ``playground-lead-api.routes.campaigns``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_GOALS``
    Config: ``playground-lead-api.routes.goals``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_LEADS``
    Config: ``playground-lead-api.routes.leads``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_OPPORTUNITIES``
    Config: ``playground-lead-api.routes.opportunities``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_PLANS``
    Config: ``playground-lead-api.routes.plans``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_REGIONS``
    Config: ``playground-lead-api.routes.regions``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_REPORTS``
    Config: ``playground-lead-api.routes.reports``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_SOURCES``
    Config: ``playground-lead-api.routes.sources``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_TASKS``
    Config: ``playground-lead-api.routes.tasks``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_TEAMS``
    Config: ``playground-lead-api.routes.teams``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_API_ROUTES_TEAMMATES``
    Config: ``playground-lead-api.routes.teammates``

    Type: ``bool``

    Default: ``true``


Installation
^^^^^^^^^^^^

NOTE: This package requires playground-lead.

.. code-block:: bash

    composer require gammamatrix/playground-lead-api


playground-lead-resource
--------------------------

Provides an API and a Laravel Blade UI for the Playground Project Management System.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-lead-resource/develop/resources/docs/artisan-about-playground-lead-resource.png
   :align: center

   ``artisan about`` for playground-lead-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-lead-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-lead-resource
    Wiki on GitHub
        https://github.com/gammamatrix/playground-lead-resource/wiki


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-lead-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-lead-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-lead-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-lead-resource/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Lead\Resource\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

If you do not want to use the flexible policies available in Playground, you may publish the config and/or routes to your base application and customize them and the middleware.

The mapping for models to policies is set in `config/playground-lead-resource.php <https://github.com/gammamatrix/playground-lead-resource/blob/develop/config/playground-lead-resource.php>`_ (may also be published).

If you wish to use your own policies, copy from `src/Policies <https://github.com/gammamatrix/playground-lead-resource/tree/develop/src/Policies>`_.


``PLAYGROUND_LEAD_RESOURCE_MIDDLEWARE_DEFAULT``
    Config: ``playground-lead-resource.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_LEAD_RESOURCE_MIDDLEWARE_USER``
    Config: ``playground-lead-resource.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_LEAD_RESOURCE_MIDDLEWARE_GUEST``
    Config: ``playground-lead-resource.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``


Loading
"""""""

``PLAYGROUND_LEAD_RESOURCE_LOAD_POLICIES``
    Config: ``playground-lead-resource.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_LOAD_ROUTES``
    Config: ``playground-lead-resource.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_LOAD_VIEWS``
    Config: ``playground-lead-resource.middleware.load.views``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_LEAD_RESOURCE_ROUTES_CAMPAIGNS``
    Config: ``playground-lead-resource.routes.campaigns``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_GOALS``
    Config: ``playground-lead-resource.routes.goals``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_LEADS``
    Config: ``playground-lead-resource.routes.leads``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_OPPORTUNITIES``
    Config: ``playground-lead-resource.routes.opportunities``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_PLANS``
    Config: ``playground-lead-resource.routes.plans``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_REGIONS``
    Config: ``playground-lead-resource.routes.regions``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_REPORTS``
    Config: ``playground-lead-resource.routes.reports``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_SOURCES``
    Config: ``playground-lead-resource.routes.sources``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_TASKS``
    Config: ``playground-lead-resource.routes.tasks``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_TEAMS``
    Config: ``playground-lead-resource.routes.teams``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_ROUTES_TEAMMATES``
    Config: ``playground-lead-resource.routes.teammates``

    Type: ``bool``

    Default: ``true``


Sitemap
"""""""

``PLAYGROUND_LEAD_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-lead-resource.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-lead-resource.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_SITEMAP_USER``
    Config: ``playground-lead-resource.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_LEAD_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-lead-resource.sitemap.view``

    Type: ``string``

    Default: ``playground-lead-resource::sitemap``

    Description: This blade file will be included on the application sitemap.


UI
""

``PLAYGROUND_LEAD_RESOURCE_BLADE``
    Config: ``playground-lead-resource.blade``

    Type: ``string``

    Default: ``playground-lead-resource::``

    Description: Sets the view namespace for the package.

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-lead.

.. code-block:: bash

    composer require gammamatrix/playground-lead-resource
