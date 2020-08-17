.. Bip documentation master file, created by
   sphinx-quickstart on Fri Jul 27 08:36:06 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Bip's documentation!
###############################

Bip is a project which aims to simplify the usage of python for interacting
with IDA. Its main goals are to facilitate the usage of python in the
interactive console of IDA and the writing of plugins. In a more general way
the goal is to automate recurrent tasks done through the python API.
Bip is also developed to provide a more object oriented, a "python-like"
API and a *real* documentation.

This code is not complete, and a lot of features are still missing. Development
is prioritized on what people ask for and what the developers use, so do not
hesitate to make PR, Feature Request and Issues (including for the
documentation), see :ref:`general-contrib` for more information.

This documentation is split in several parts. The `General`_ part should allow
you to start with the project including the install (:ref:`general-install`)
and an overview (:ref:`general-overview`) which explain how to use it.
The :ref:`general-archi` allows to get a better understanding of how the
project works and was intended to be used.

The main part of the documentation is split in the three parts of
bip: :ref:`index-base`
containing the basic interfaces, the :ref:`index-hexrays` for manipulating
hexrays functions and the :ref:`index-gui` containing interface with the
graphics and explaining how to developed plugins. This is mainly
autodocumentation of bip objects with precisions about usage and potentially
internals when necessary.

General
=======

.. toctree::
    :maxdepth: 3

    general/install
    general/overview
    general/archi
    general/contribution
    general/changelog

.. _index-base:

Base interface (``bip.base``)
=============================

This regroup the part about the base interface on top of the IDA basic API.
All classes in this part are regroup in the ``bip.base`` module.

.. toctree::
    :maxdepth: 2

    base/elt
    base/instr
    base/data
    base/func
    base/xref
    base/struct
    base/enum
    base/type
    base/bipidb
    base/bipida

.. _index-hexrays:

Hexrays interface (``bip.hexrays``)
===================================

This regroup the interface on top of the IDA Hexrays API, in particular it
allows to visit the AST generated for the functions. This module will be
useful only if the decompiler for the binary exist and is installed.

.. toctree::
    :maxdepth: 2

    hexrays/cfunc
    hexrays/lvar
    hexrays/astnodes
    hexrays/cnode
    hexrays/visit_hx

.. _index-gui:

GUI & Plugins interface (``bip.gui``)
=====================================

This part regroup all the functions and classes made for interfacing with the
UI and events of IDA. The most important part of this module is probably the
:class:`BipPlugin` which allow to create plugins and to define actions in IDA.
While bip can be used in normal IDA plugin and scripts, the :class:`BipPlugin`
is the central element for interfacing with the GUI using bip.

.. toctree::
    :maxdepth: 2

    gui/plugin
    gui/plgmanager
    gui/activity
    gui/userselect

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

