Admin Packages
==============

The Playground Admin provides a user and setting management system that may be
consumed by a Laravel application or served as JSON from a Laravel based API or
Resource.

.. contents:: Table of Contents

playground-admin
^^^^^^^^^^^^^^^^

Provides the models for playground-admin-resource.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-admin/develop/resources/docs/artisan-about-playground-admin.png
..    :align: center

..    ``artisan about`` for playground-admin

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-admin
    Source on GitHub
        https://github.com/gammamatrix/playground-admin


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Admin\ServiceProvider" --tag="playground-config"


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Migrations
""""""""""

All migrations are disabled by default.

See the contents of the published config file: `database/migrations <https://github.com/gammamatrix/playground-admin/tree/develop/database/migrations>`_
- NOTE: There are 15 tables that will be created, they do have indexes and unique constraints defined; however, this release does not have the foreign key constraint migrations included at this time.


* If you do not wish to publish the migrations to your application, you may use the Environment Variable: ``PLAYGROUND_ADMIN_LOAD_MIGRATIONS`` in your ``.env``.

``PLAYGROUND_ADMIN_LOAD_MIGRATIONS``
    Config: ``playground-admin-resource.middleware.default``

    Type: ``bool``

    Default: ``false``

    Description: The loading option for migrations does not take effect if the migrations have been published to your app. The control for loading is handled in the package `ServiceProvider <https://github.com/gammamatrix/playground-admin/blob/develop/src/ServiceProvider.php>`_.

You can publish the migrations file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Admin\ServiceProvider" --tag="playground-migrations"

Installation
^^^^^^^^^^^^

NOTE: This package is required by playground-admin-api and playground-admin-resource.

* playground-admin-api has not been published.


.. code-block:: bash

    composer require gammamatrix/playground-admin

playground-admin-resource
^^^^^^^^^^^^^^^^^^^^^^^^^

Provides an API and a Laravel Blade UI.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-admin-resource/develop/resources/docs/artisan-about-playground-admin-resource.png
..    :align: center

..    ``artisan about`` for playground-admin-resource

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-admin-resource
    Source on GitHub
        https://github.com/gammamatrix/playground-admin-resource

