Site
====

The Playground Site Blade package for `Laravel <https://laravel.com/docs/11.x>`_ applications.

This package provides Controllers and Blade UI handling:

* Bootstrap Theme Handling
* Dashboard
* Home and Index
* Sitemap
* Welcome

.. contents:: Table of Contents

playground-site-blade
---------------------

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/artisan-about-playground-site-blade.png
   :align: center

   ``artisan about`` for playground-site-blade

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-site-blade
    Source on GitHub
        https://github.com/gammamatrix/playground-site-blade


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Site\Blade\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

Authentication and Authorization
""""""""""""""""""""""""""""""""

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_DEFAULT``
    Config: ``playground-site-blade.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_AUTH``
    Config: ``playground-site-blade.middleware.auth``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_GUEST``
    Config: ``playground-site-blade.middleware.guest``

    Type: ``string|array``

    Default: ``['web']``


Dashboard
"""""""""

``PLAYGROUND_SITE_BLADE_DASHBOARD_ENABLE``
    Config: ``playground-site-blade.middleware.dashboard.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_GUEST``
    Config: ``playground-site-blade.middleware.dashboard.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_USER``
    Config: ``playground-site-blade.middleware.dashboard.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_VIEW``
    Config: ``playground-site-blade.middleware.dashboard.view``

    Type: ``string``

    Default: ``playground-site-blade::dashboard``

Loading
"""""""

``PLAYGROUND_SITE_BLADE_LOAD_VIEWS``
    Config: ``playground-site-blade.middleware.load.views``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_LOAD_ROUTES``
    Config: ``playground-site-blade.middleware.load.routes``

    Type: ``bool``

    Default: ``true``


Routes
""""""

``PLAYGROUND_SITE_BLADE_ROUTES_ABOUT``
    Config: ``playground-site-blade.middleware.routes.about``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_BOOTSTRAP``
    Config: ``playground-site-blade.middleware.routes.bootstrap``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_DASHBOARD``
    Config: ``playground-site-blade.middleware.routes.dashboard``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_HOME``
    Config: ``playground-site-blade.middleware.routes.home``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_INDEX``
    Config: ``playground-site-blade.middleware.routes.index``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_SITEMAP``
    Config: ``playground-site-blade.middleware.routes.sitemap``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_THEME``
    Config: ``playground-site-blade.middleware.routes.theme``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_WELCOME``
    Config: ``playground-site-blade.middleware.routes.welcome``

    Type: ``bool``

    Default: ``true``


Installation
^^^^^^^^^^^^

NOTE: This package requires playground-matrix.

.. code-block:: bash

    composer require gammamatrix/playground-site-blade

Sitemap
"""""""

``PLAYGROUND_SITE_BLADE_SITEMAP_ENABLE``
    Config: ``playground-site-blade.middleware.sitemap.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_SITEMAP_GUEST``
    Config: ``playground-site-blade.middleware.sitemap.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_SITEMAP_USER``
    Config: ``playground-site-blade.middleware.sitemap.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_SITEMAP_VIEW``
    Config: ``playground-site-blade.middleware.sitemap.view``

    Type: ``string``

    Default: ``playground-site-blade::sitemap``

    Description: This blade file will be included on the application sitemap.


UI
""

``PLAYGROUND_MATRIX_RESOURCE_BLADE``
    Config: ``playground-site-blade.blade``

    Type: ``string``

    Default: ``playground-site-blade::``

    Description: Sets the view namespace for the package.


Installation
^^^^^^^^^^^^

.. code-block:: bash

    composer require gammamatrix/playground-site-blade

