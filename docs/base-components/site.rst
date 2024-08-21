Site
####

The Playground Site Blade package for `Laravel <https://laravel.com/docs/11.x>`_ applications.

This package provides Controllers and Blade UI handling:

* Bootstrap Theme Handling
* Dashboard
* Home and Index
* Sitemap
* Welcome

.. contents:: Table of Contents


playground-site-blade


.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/artisan-about-playground-site-blade.png
   :align: center

   ``artisan about`` for playground-site-blade

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-site-blade
    Source on GitHub
        https://github.com/gammamatrix/playground-site-blade


.. _playground-site-blade Configuration:

Configuration
*********************

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Site\Blade\ServiceProvider" --tag="playground-config"

.. _playground-site-blade Environment Variables:

Environment Variables
*********************

.. _playground-site-blade Authentication and Authorization:

Authentication and Authorization
================================================

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_DEFAULT``
    Config: ``playground-site-blade.middleware.default``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_DASHBOARD``
    Config: ``playground-site-blade.middleware.dashboard``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_HOME``
    Config: ``playground-site-blade.middleware.home``

    Type: ``string|array``

    Default: ``['web', 'auth']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_PAGE``
    Config: ``playground-site-blade.middleware.page``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_SITEMAP``
    Config: ``playground-site-blade.middleware.sitemap``

    Type: ``string|array``

    Default: ``['web']``

``PLAYGROUND_SITE_BLADE_MIDDLEWARE_WELCOME``
    Config: ``playground-site-blade.middleware.welcome``

    Type: ``string|array``

    Default: ``['web']``

.. _playground-site-blade Dashboard:

Dashboard
========================

``PLAYGROUND_SITE_BLADE_DASHBOARD_ENABLE``
    Config: ``playground-site-blade.dashboard.enable``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_GUEST``
    Config: ``playground-site-blade.dashboard.guest``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_USER``
    Config: ``playground-site-blade.dashboard.user``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_DASHBOARD_VIEW``
    Config: ``playground-site-blade.dashboard.view``

    Type: ``string``

    Default: ``playground-site::dashboard``

.. _playground-site-blade Loading:

Loading
========================

``PLAYGROUND_SITE_BLADE_LOAD_VIEWS``
    Config: ``playground-site-blade.load.views``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_LOAD_ROUTES``
    Config: ``playground-site-blade.load.routes``

    Type: ``bool``

    Default: ``true``

.. _playground-site-blade Routes:

Routes
========================

``PLAYGROUND_SITE_BLADE_ROUTES_ABOUT``
    Config: ``playground-site-blade.routes.about``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_BOOTSTRAP``
    Config: ``playground-site-blade.routes.bootstrap``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_DASHBOARD``
    Config: ``playground-site-blade.routes.dashboard``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_HOME``
    Config: ``playground-site-blade.routes.home``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_INDEX``
    Config: ``playground-site-blade.routes.index``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_PAGE``
    Config: ``playground-site-blade.routes.page``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_SITEMAP``
    Config: ``playground-site-blade.routes.sitemap``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_THEME``
    Config: ``playground-site-blade.routes.theme``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_SITE_BLADE_ROUTES_WELCOME``
    Config: ``playground-site-blade.routes.welcome``

    Type: ``bool``

    Default: ``true``

.. _playground-site-blade Sitemap:

Sitemap
========================

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

.. _playground-site-blade UI:

UI
========================

``PLAYGROUND_MATRIX_RESOURCE_BLADE``
    Config: ``playground-site-blade.blade``

    Type: ``string``

    Default: ``playground-site-blade::``

    Description: Sets the view namespace for the package.

.. _playground-site-blade Installation:

Installation
*********************

.. code-block:: bash

    composer require gammamatrix/playground-site-blade


Sitemap
*********************

.. list-table::
   :width: 100%
   :class: borderless

   * - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-login.png

        Fig 1. Sitemap for `playground-login-blade <https://github.com/gammamatrix/playground-login-blade/blob/develop/resources/views/sitemap.blade.php>`_

     - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-site.png

        Fig 2. Sitemap for `playground-site-blade <https://github.com/gammamatrix/playground-site-blade/blob/develop/resources/views/sitemap.blade.php>`_

   * - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-admin.png

        Fig 3. Sitemap for `playground-admin-resource <https://github.com/gammamatrix/playground-admin-resource/blob/develop/resources/views/sitemap.blade.php>`_

     - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-cms.png

        Fig 4. Sitemap for `playground-cms-resource <https://github.com/gammamatrix/playground-cms-resource/blob/develop/resources/views/sitemap.blade.php>`_

   * - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-crm.png

        Fig 5. Sitemap for `playground-crm-resource <https://github.com/gammamatrix/playground-crm-resource/blob/develop/resources/views/sitemap.blade.php>`_

     - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-directory.png

        Fig 6. Sitemap for `playground-directory-resource <https://github.com/gammamatrix/playground-directory-resource/blob/develop/resources/views/sitemap.blade.php>`_

   * - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-matrix.png

        Fig 7. Sitemap for `playground-matrix-resource <https://github.com/gammamatrix/playground-matrix-resource/blob/develop/resources/views/sitemap.blade.php>`_

     - .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-sitemap-lead.png

        Fig 8. Sitemap for `playground-lead-resource <https://github.com/gammamatrix/playground-lead-resource/blob/develop/resources/views/sitemap.blade.php>`_

Themes
*********************

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground-site-blade/develop/resources/docs/playground-site-blade-theme-select.png
   :align: center

   Selecting dark mode with the playground-site-blade package.
