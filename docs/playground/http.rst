Http
====

The Playground Matrix provides controller and request handling.

.. contents:: Table of Contents


playground-http
---------------

Provides the base classes, concerns, contracts and translations for API and Resource packages.

.. .. figure:: https://raw.githubusercontent.com/gammamatrix/playground-http/develop/resources/docs/artisan-about-playground-http.png
..    :align: center

..    ``artisan about`` for playground-http

.. admonition:: Package Information

    Packagist
        https://packagist.org/packages/gammamatrix/playground-http
    Source on GitHub
        https://github.com/gammamatrix/playground-http


Configuration
^^^^^^^^^^^^^

You can publish the configuration file with:

.. code-block:: bash

    php artisan vendor:publish --provider="Playground\Http\ServiceProvider" --tag="playground-config"

Environment Variables
^^^^^^^^^^^^^^^^^^^^^

``PLAYGROUND_HTTP_LOAD_TRANSLATIONS``
    Config: ``playground-http.load.translations``

    Type: ``bool``

    Default: ``true``

``PLAYGROUND_HTTP_PURIFIER_IFRAMES``
    Config: ``playground-http.purifier.iframes``

    Type: ``string`` Regular Expression to match streaming providers.

    Default: ``%^(https?:)?(\/\/www\.youtube(?:-nocookie)?\.com\/embed\/|\/\/player\.vimeo\.com\/)%``

    Example: ``null``

``PLAYGROUND_HTTP_PURIFIER_PATH``
    Config: ``playground-http.purifier.path``

    Type: ``string``

    Default: ``''``

    Example: ``/tmp``


.. code-block:: php

    <?php
    /**
    * Playground
    */
    namespace Playground\Http\Requests\Concerns;

    use HTMLPurifier;

    /**
    * \Playground\Http\Requests\Concerns\StoreContent
    */
    trait StoreContent
    {
        protected ?HTMLPurifier $purifier = null;

        protected ?string $safeIframeRegexp = '%^(https?:)?(\/\/www\.youtube(?:-nocookie)?\.com\/embed\/|\/\/player\.vimeo\.com\/)%';

        /**
        * Exorcise all html from the string.
        *
        * @uses \htmlspecialchars()
        * @uses \strip_tags()
        */
        public static function exorcise(mixed $content): string
