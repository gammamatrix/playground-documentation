Playground Base Package
=======================

This is the base package for Playground.

This package provides model handling for `Laravel <https://laravel.com/docs/11.x>`_ packages.

* Playground allows using `Laravel ordered UUIDs <https://laravel.com/docs/11.x/strings#method-str-ordered-uuid>`_ for primary keys.
* The configuration in Playground and subpackages permits defining the user model, table and primary key type: `increments` or `uuid`.
* Packages are compatible and tested with and without: middleware, roles, policies, privileges, Sanctum...


.. contents:: Table of Contents


playground
----------

Provides the base system for Playground under Laravel.

.. figure:: https://raw.githubusercontent.com/gammamatrix/playground/develop/resources/docs/artisan-about-playground.png
   :align: center

   ``artisan about`` for playground

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground
    Source on GitHub
        https://github.com/gammamatrix/playground


Environment Variables
^^^^^^^^^^^^^^^^^^^^^

``PLAYGROUND_PACKAGES``
    Config: ``playground.packages``

    Type: ``string`` Expects a CSV string. Spaces between packages is acceptable.

    Default: ``playground``

    Example: ``playground,playground-auth,playground-blade,playground-http,playground-login-blade,playground-site-blade,playground-admin-resource,playground-cms-resource,playground-test``

    Example: ``playground, playground-auth, playground-blade ,playground-http, playground-login-blade, playground-site-blade, playground-admin-resource, playground-cms-resource, playground-test``

    Description: You may optionally include Playground based packages in this variable. If included, and using a Blade UI and the Sitemap feature, these packages will have their respective sitemaps rendered.

    NOTE: See ``PLAYGROUND_AUTH_PACKAGES`` for loading required security privileges for relevant packages.

``PLAYGROUND_DATE_SQL``
    Config: ``playground.date``

    Type: ``string``

    Default: ``Y-m-d H:i:s``

    Description: This date format is only necessary when the date needs to be formatted for database insertion; otherwise, Carbon handles the date.

.. code-block:: bash
    :caption: These environment variables are used in `site-playground [on GitHub] <https://github.com/gammamatrix/site-playground>`_.

    ################################################################################
    #
    # Playground
    #
    ################################################################################
    #
    PLAYGROUND_PACKAGES=playground,playground-auth,playground-blade,playground-http,playground-login-blade,playground-site-blade,playground-admin-resource,playground-cms-resource,playground-test
    #
    PLAYGROUND_ADMIN_LOAD_MIGRATIONS=true
    #
    PLAYGROUND_AUTH_PACKAGES=playground-admin-resource,playground-cms-resource,playground-login-blade,playground-site-blade
    #
    PLAYGROUND_CMS_LOAD_MIGRATIONS=true
    #
    PLAYGROUND_AUTH_DEBUG=true


Installation
^^^^^^^^^^^^

NOTE: Typically, this package is automatically included when using other Playground packages.

It would only need to be installed if creating a new Playground based package.

.. code-block:: bash

    composer require gammamatrix/playground

