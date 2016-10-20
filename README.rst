Config Transform
================

Config Transform is a library for deserializing configuration files from a
``map[string]interface{}`` to a struct type. It is commonly used with JSON and
YAML configuration files.

Features include:

* generate documentation from comments on the ``struct``
* custom deserialization of user defined types
* useful error messages when transformation fails
* additional user-defined field validation

.. image:: https://godoc.org/github.com/dnephin/configtf?status.svg
    :target: http://godoc.org/github.com/dnephin/configtf

.. image:: https://circleci.com/gh/dnephin/configtf/tree/master.svg?style=shield
    :target: https://circleci.com/gh/dnephin/configtf/tree/master


Why configtf?
-------------

Both ``encoding/json`` and ``go-yaml`` provide functions for deserializing from
a config file, but each have their significant shortcomings:

* the error messages returned by ``encoding/json`` do not include enough
  information to actually find and fix the error
* ``go-yaml`` does not support polymorphic types
* supporting multiple config formats (json, yaml, ini, toml, etc) requires that
  you annotate your structs for each format
* no support for generated documentation
* no user-defined type validation
