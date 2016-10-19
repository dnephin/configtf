Config Transform
================

Transform is a library for deserializing configuration files from a
``map[string]interface{}`` to a struct type. It is commonly used with JSON and
YAML configuration files.

Features include:

* generate documentation from comments on the ``struct``
* custom deserialization of user defined types
* useful error messages when transformation fails

Why transform?
--------------

Both ``encoding/json`` and ``go-yaml`` provide functions for deserializing from
a config file, but each have their significant shortcomings:

* the error messages returned by ``encoding/json`` do not include enough
  information to actually find and fix the error
* ``go-yaml`` does not support polymorphic types
* ...
