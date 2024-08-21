Installation
############

.. Attention::

    Playground v73.0 is currently unstable.

    * See the `Playground Project Status Board for v73.0.0 (on GitHub Projects) <https://github.com/users/gammamatrix/projects/1/views/2?sliceBy%5BcolumnId%5D=Repository>`_.

    * For PHP based applications, Playground utilizes the :term:`Laravel`.
    * For ECMAScript based applications, Playground may use any of :term:`Angular`, :term:`React` or :term:`Vue`.
    * For UI/UX , Playground may use any of :term:`Bootstrap`, :term:`Angular Material` or :term:`Tailwind`.


Sites and packages may be set up with :term:`Composer`.

.. code:: console

    composer install


Packages may be added to Laravel sites with:

.. code:: console

    composer require gammamatrix/playground

.. _howto_upgrade:

How to upgrade
**************

Currently, Playground utilizes Laravel v11 for the underlying framework.

.. code:: console

    composer update
