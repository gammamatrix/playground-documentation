Matrix Packages
===============

The Playground Matrix provides a project management system that may be consumed
by a Laravel application or served as JSON from a Laravel based API or Resource.

.. contents:: Table of Contents


playground-matrix
-----------------

Provides the models for playground-matrix-api and playground-matrix-resource.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-matrix/develop/resources/docs/artisan-about-playground-matrix.png
   :align: center

   ``artisan about`` for playground-matrix

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-matrix
    Source on GitHub
        https://github.com/gammamatrix/playground-matrix


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Matrix\ServiceProvider" --tag="playground-config"


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Migrations
""""""""""

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-matrix/tree/develop/database/migrations>`_
- NOTE: There are 15 tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_MATRIX_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_MATRIX_LOAD_MIGRATIONS``
    Config: ``playground-matrix-resource.middleware.default``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package [ServiceProvider.](src/ServiceProvider.php)

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Matrix\ServiceProvider" --tag="playground-migrations"

Installation
^^^^^^^^^^^^

NOTE: This package is required by playground-matrix-api and playground-matrix-resource.

.. code-block:: bash

    composer require gammamatrix/playground-matrix


playground-matrix-api
---------------------

Provides an API, without a UI for the Playground Project Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-matrix-api/develop/apis/docs/artisan-about-playground-matrix-api.png
..    :align: center

..    ``artisan about`` for playground-matrix-api

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-matrix-api
    Source on GitHub
        https://github.com/gammamatrix/playground-matrix-api


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-matrix-api/swagger.json provided in the repository <https://github.com/gammamatrix/playground-matrix-api/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-matrix-api/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-matrix-api/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Matrix\Api\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

``PLAYGROUND_MATRIX_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-matrix-api.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_MATRIX_API_MIDDLEWARE_USER``
    Config: ``playground-matrix-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_MATRIX_API_MIDDLEWARE_GUEST``
    Config: ``playground-matrix-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``


Loading
"""""""

``PLAYGROUND_MATRIX_API_LOAD_POLICIES``
    Config: ``playground-matrix-api.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_LOAD_ROUTES``
    Config: ``playground-matrix-api.middleware.load.routes``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_MATRIX_API_ROUTES_BACKLOGS``
    Config: ``playground-matrix-api.middleware.routes.backlogs``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_BOARDS``
    Config: ``playground-matrix-api.middleware.routes.boards``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_EPICS``
    Config: ``playground-matrix-api.middleware.routes.epics``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_FLOWS``
    Config: ``playground-matrix-api.middleware.routes.flows``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_MILESTONES``
    Config: ``playground-matrix-api.middleware.routes.milestones``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_NOTES``
    Config: ``playground-matrix-api.middleware.routes.notes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_PROJECTS``
    Config: ``playground-matrix-api.middleware.routes.projects``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_RELEASES``
    Config: ``playground-matrix-api.middleware.routes.releases``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_ROADMAPS``
    Config: ``playground-matrix-api.middleware.routes.roadmaps``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_SOURCES``
    Config: ``playground-matrix-api.middleware.routes.sources``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_SPRINTS``
    Config: ``playground-matrix-api.middleware.routes.sprints``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_TAGS``
    Config: ``playground-matrix-api.middleware.routes.tags``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_TEAMS``
    Config: ``playground-matrix-api.middleware.routes.teams``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_TICKETS``
    Config: ``playground-matrix-api.middleware.routes.tickets``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_API_ROUTES_VERSIONS``
    Config: ``playground-matrix-api.middleware.routes.versions``

    Type: ``bool``

    Default: ``true``

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-matrix.

.. code-block:: bash

    composer require gammamatrix/playground-matrix-api


playground-matrix-resource
--------------------------

Provides an API and a Laravel Blade UI for the Playground Project Management System.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-matrix-resource/develop/resources/docs/artisan-about-playground-matrix-resource.png
   :align: center

   ``artisan about`` for playground-matrix-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-matrix-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-matrix-resource
    Wiki on GitHub
        https://github.com/gammamatrix/playground-matrix-resource/wiki


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-matrix-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-matrix-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-matrix-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-matrix-resource/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Matrix\Resource\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

If you do not want to use the flexible policies available in Playground, you may publish the config and/or routes to your base application and customize them and the middleware.

The mapping for models to policies is set in `config/playground-matrix-resource.php <https://github.com/gammamatrix/playground-matrix-resource/blob/develop/config/playground-matrix-resource.php>`_ (may also be published).

If you wish to use your own policies, copy from `src/Policies <https://github.com/gammamatrix/playground-matrix-resource/tree/develop/src/Policies>`_.


``PLAYGROUND_MATRIX_RESOURCE_MIDDLEWARE_DEFAULT``
    Config: ``playground-matrix-resource.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_MATRIX_RESOURCE_MIDDLEWARE_USER``
    Config: ``playground-matrix-resource.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_MATRIX_RESOURCE_MIDDLEWARE_GUEST``
    Config: ``playground-matrix-resource.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``


Loading
"""""""

``PLAYGROUND_MATRIX_RESOURCE_LOAD_POLICIES``
    Config: ``playground-matrix-resource.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_LOAD_ROUTES``
    Config: ``playground-matrix-resource.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_LOAD_VIEWS``
    Config: ``playground-matrix-resource.middleware.load.views``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_MATRIX``
    Config: ``playground-matrix-resource.middleware.routes.matrix``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_BACKLOGS``
    Config: ``playground-matrix-resource.middleware.routes.backlogs``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_BOARDS``
    Config: ``playground-matrix-resource.middleware.routes.boards``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_EPICS``
    Config: ``playground-matrix-resource.middleware.routes.epics``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_FLOWS``
    Config: ``playground-matrix-resource.middleware.routes.flows``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_MILESTONES``
    Config: ``playground-matrix-resource.middleware.routes.milestones``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_NOTES``
    Config: ``playground-matrix-resource.middleware.routes.notes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_PROJECTS``
    Config: ``playground-matrix-resource.middleware.routes.projects``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_RELEASES``
    Config: ``playground-matrix-resource.middleware.routes.releases``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_ROADMAPS``
    Config: ``playground-matrix-resource.middleware.routes.roadmaps``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_SOURCES``
    Config: ``playground-matrix-resource.middleware.routes.sources``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_SPRINTS``
    Config: ``playground-matrix-resource.middleware.routes.sprints``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_TAGS``
    Config: ``playground-matrix-resource.middleware.routes.tags``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_TEAMS``
    Config: ``playground-matrix-resource.middleware.routes.teams``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_TICKETS``
    Config: ``playground-matrix-resource.middleware.routes.tickets``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_ROUTES_VERSIONS``
    Config: ``playground-matrix-resource.middleware.routes.versions``

    Type: ``bool``

    Default: ``true``


Sitemap
"""""""

``PLAYGROUND_MATRIX_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-matrix-resource.middleware.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-matrix-resource.middleware.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_SITEMAP_USER``
    Config: ``playground-matrix-resource.middleware.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_MATRIX_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-matrix-resource.middleware.sitemap.view``

    Type: ``string``

    Default: ``playground-matrix-resource::sitemap``

    Description: This blade file will be included on the application sitemap.


UI
""

``PLAYGROUND_MATRIX_RESOURCE_BLADE``
    Config: ``playground-matrix-resource.blade``

    Type: ``string``

    Default: ``playground-matrix-resource::``

    Description: Sets the view namespace for the package.

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-matrix.

.. code-block:: bash

    composer require gammamatrix/playground-matrix-resource
