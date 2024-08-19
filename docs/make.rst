Playground Make Packages
########################

Every organization has different specific needs. **Playground Make** provides abilities and recipes to rebuild PHP and ECMAScript applications in seconds, tailored to the desired requirements and features of a project.

PHP Applications
****************


playground-make
===============

The primary commands, under playground-make, are :ref:`playground:make:package<playground-make-package>` and :ref:`playground:make:model<playground-make-model>`.

- They utilize all the other commands when generating packages.


.. code-block:: console

    ➜  site-playground-make git:(master) artisan playground:make

    Laravel Framework 11.20.0

    Usage:
        command [options] [arguments]

    Options:
        -h, --help            Display help for the given command. When no command is given display help for the list command
        -q, --quiet           Do not output any message
        -V, --version         Display this application version
            --ansi|--no-ansi  Force (or disable --no-ansi) ANSI output
        -n, --no-interaction  Do not ask any interactive question
            --env[=ENV]       The environment the command should run under
        -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

    Available commands for the "playground:make" namespace:
        playground:make:blade       Create a new blade template
        playground:make:controller  Create a new controller class
        playground:make:factory     Create a new model factory
        playground:make:migration   Create a new migration file
        playground:make:model       Create a new Eloquent model class
        playground:make:package     Create a package
        playground:make:policy      Create a new policy class
        playground:make:request     Create a new form request class
        playground:make:resource    Create a new resource
        playground:make:route       Create a new route group
        playground:make:seeder      Create a new seeder class
        playground:make:swagger     Create a new docs group
        playground:make:test        Create a new test case


playground-make-blade
=====================


playground-make-controller
==========================

playground-make-policy
----------------------

playground-make-request
-----------------------

playground-make-resource
------------------------

playground-make-route
---------------------


playground-make-model
=====================

playground-make-factory
-----------------------

playground-make-migration
-------------------------

playground-make-seeder
----------------------


playground-make-package
=======================

.. code-block:: console

    ➜  site-playground-make git:(master) artisan help playground:make:package

    Description:
        Create a package

    Usage:
        playground:make:package [options] [--] [<name>]

    Arguments:
        name                                     The name of the package

    Options:
        -f, --force                              Create the class even if the package already exists
        -i, --interactive                        Use interactive mode to create the class even for the package
        -m, --model[=MODEL]                      The model that the package applies to
            --module[=MODULE]                    The module that the package belongs to
            --namespace[=NAMESPACE]              The namespace of the package
            --type[=TYPE]                        The configuration type of the package
            --organization[=ORGANIZATION]        The organization of the package
            --package[=PACKAGE]                  The package of the package
            --preload                            Preload the existing configuration file for the package
            --playground                         Allow the package to use Playground features
            --skeleton                           Create the skeleton for the package type
            --class[=CLASS]                      The class name of the package
            --extends[=EXTENDS]                  The class that gets extended for the package
            --file[=FILE]                        The configuration file of the package
            --model-file[=MODEL-FILE]            The configuration file of the model for the package
            --blade                              The package will have blade templates
            --controllers                        The package will have controllers
            --covers                             Use CoversClass for code coverage
            --factories                          The package will have model factories
            --migrations                         The package will have model migrations
            --models                             The package will have models
            --policies                           The package will have policies
            --requests                           The package will have requests
            --routes                             The package will have routes
            --license[=LICENSE]                  The package license
            --email[=EMAIL]                      The package organization email
            --package-version[=PACKAGE-VERSION]  The package version
            --packagist[=PACKAGIST]              The package packagist name in composer.json
            --build                              Build the package controllers, policies, requests and routes for the models
            --revision                           Allow the package to use revision features
            --swagger                            Build the package the Swagger documentation
            --test                               Create the unit and feature tests for the package
            --api                                Generate an API controller class when creating the model. Requires --controllers option
        -r, --resource                           Generate a resource controller class when creating the model. Requires --controllers option
            --model-package[=MODEL-PACKAGE]      Provide a model package configuration to import into an API or Resource package.
        -h, --help                               Display help for the given command. When no command is given display help for the list command
        -q, --quiet                              Do not output any message
        -V, --version                            Display this application version
            --ansi|--no-ansi                     Force (or disable --no-ansi) ANSI output
        -n, --no-interaction                     Do not ask any interactive question
            --env[=ENV]                          The environment the command should run under
        -v|vv|vvv, --verbose                     Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug



playground-make-postman
=======================

.. Note::

    - The Postman code has not been published to GitHub yet.

playground-make-swagger
=======================

.. Note::

    - The Swagger cli package used to build documentation has been deprecated. `Redocly provides a replacement [GH-2 on GitHub] <https://github.com/gammamatrix/playground-make-swagger/issues/2>`_.


playground-make-test
=======================

ECMAScript Applications
***********************

playground-make-angular
=======================

playground-make-react
=====================


playground-make-vue
===================

Developer Notes
***************

.. Note::

    For now, the Playground Make Packages will not be put into Packagist.

    * The `Swagger <https://swagger.io/>`_ (`OpenAPI <https://www.openapis.org/>`_) docs and `Postman <https://postman.com/gammamatrix/>`_ packages are incomplete.
