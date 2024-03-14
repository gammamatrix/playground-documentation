CMS Packages
============

The Playground CMS provides a content management system, with pages and
snippets, that may be consumed by a Laravel application or served as JSON from a Laravel based API or Resource.

Features:

* Pages and Snippets support revisions.
* Start, Embargo, End and Planned dates are available for controlling content releases.
* Supports custom authorization for each page and snippet: Owner, Groups, po, pg, pw, only_admin, only_user, only_guest, allow_public
* Multiple page types to support magazines, books, articles and more.

.. contents:: Table of Contents


playground-cms
--------------

Provides the models for playground-cms-api and playground-cms-resource.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms/develop/resources/docs/artisan-about-playground-cms.png
..    :align: center

..    ``artisan about`` for playground-cms

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms
    Source on GitHub
        https://github.com/gammamatrix/playground-cms


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\ServiceProvider" --tag="playground-config"


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Migrations
""""""""""

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-cms/tree/develop/database/migrations>`_
- NOTE: There are 15 tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_CMS_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_CMS_LOAD_MIGRATIONS``
    Config: ``playground-cms-resource.middleware.default``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\ServiceProvider" --tag="playground-migrations"

Installation
^^^^^^^^^^^^

NOTE: This package is required by playground-cms-api and playground-cms-resource.

.. code-block:: bash

    composer require gammamatrix/playground-cms


playground-cms-api
------------------

.. Attention:: This package has not been published yet.

Provides an API, without a UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/apis/docs/artisan-about-playground-cms-api.png
..    :align: center

..    ``artisan about`` for playground-cms-api

.. admonition:: Package Information

    Packagist
        packagist.org/packages/gammamatrix/playground-cms-api
    Source on GitHub
        https://github.com/gammamatrix/playground-cms-api


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the gammamatrix/playground-cms-api/swagger.json provided in the repository packagist.org/packages/gammamatrix/playground-cms-api/swagger.json.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/swagger.json
    Redocly
        redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-api/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\Api\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

``PLAYGROUND_CMS_API_MIDDLEWARE_DEFAULT``
    Config: ``playground-cms-api.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_CMS_API_MIDDLEWARE_USER``
    Config: ``playground-cms-api.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_CMS_API_MIDDLEWARE_GUEST``
    Config: ``playground-cms-api.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``


Loading
"""""""

``PLAYGROUND_CMS_API_LOAD_POLICIES``
    Config: ``playground-cms-api.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_LOAD_ROUTES``
    Config: ``playground-cms-api.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_LOAD_TRANSLATIONS``
    Config: ``playground-cms-api.middleware.load.translations``

    Type: ``bool``

    Default: ``true``


Revision
""""""""

``PLAYGROUND_CMS_API_ROUTES_OPTIONAL``
    Config: ``playground-cms-api.middleware.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_REVISIONS_PAGES``
    Config: ``playground-cms-api.middleware.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_REVISIONS_SNIPPETS``
    Config: ``playground-cms-api.middleware.revisions.snippets``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_CMS_API_ROUTES_CMS``
    Config: ``playground-cms-api.middleware.routes.cms``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_ROUTES_SNIPPETS``
    Config: ``playground-cms-api.middleware.routes.snippets``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_API_ROUTES_PAGES``
    Config: ``playground-cms-api.middleware.routes.pages``

    Type: ``bool``

    Default: ``true``

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-cms.

.. code-block:: bash

    composer require gammamatrix/playground-cms-api


playground-cms-resource
-----------------------

Provides an API and a Laravel Blade UI for the Playground Content Management System.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/resources/docs/artisan-about-playground-cms-resource.png
..    :align: center

..    ``artisan about`` for playground-cms-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-cms-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-cms-resource


API Documentation
^^^^^^^^^^^^^^^^^

Documentation is generated from the `gammamatrix/playground-cms-resource/swagger.json provided in the repository <https://github.com/gammamatrix/playground-cms-resource/blob/develop/swagger.json>`_.

.. admonition:: Swagger Documentation Preview

    Swagger Editor UI
        https://editor.swagger.io/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/swagger.json
    Redocly
        https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/gammamatrix/playground-cms-resource/develop/swagger.json


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Cms\Resource\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

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


Loading
"""""""

``PLAYGROUND_CMS_RESOURCE_LOAD_POLICIES``
    Config: ``playground-cms-resource.middleware.load.policies``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_LOAD_ROUTES``
    Config: ``playground-cms-resource.middleware.load.routes``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_LOAD_VIEWS``
    Config: ``playground-cms-resource.middleware.load.views``

    Type: ``bool``

    Default: ``true``


Revision
""""""""

``PLAYGROUND_CMS_RESOURCE_ROUTES_OPTIONAL``
    Config: ``playground-cms-resource.middleware.revisions.optional``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_REVISIONS_PAGES``
    Config: ``playground-cms-resource.middleware.revisions.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_REVISIONS_SNIPPETS``
    Config: ``playground-cms-resource.middleware.revisions.snippets``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_CMS_RESOURCE_ROUTES_CMS``
    Config: ``playground-cms-resource.middleware.routes.cms``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_ROUTES_PAGES``
    Config: ``playground-cms-resource.middleware.routes.pages``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_ROUTES_SNIPPETS``
    Config: ``playground-cms-resource.middleware.routes.snippets``

    Type: ``bool``

    Default: ``true``


Sitemap
"""""""

``PLAYGROUND_CMS_RESOURCE_SITEMAP_ENABLE``
    Config: ``playground-cms-resource.middleware.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_GUEST``
    Config: ``playground-cms-resource.middleware.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_USER``
    Config: ``playground-cms-resource.middleware.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_CMS_RESOURCE_SITEMAP_VIEW``
    Config: ``playground-cms-resource.middleware.sitemap.view``

    Type: ``string``

    Default: ``playground-cms-resource::sitemap``

    Description: This blade file will be included on the application sitemap.


UI
""

``PLAYGROUND_CMS_RESOURCE_BLADE``
    Config: ``playground-cms-resource.blade``

    Type: ``string``

    Default: ``playground-cms-resource::``

    Description: Sets the view namespace for the package.

Installation
^^^^^^^^^^^^

NOTE: This package requires playground-cms.

.. code-block:: bash

    composer require gammamatrix/playground-cms-resource
