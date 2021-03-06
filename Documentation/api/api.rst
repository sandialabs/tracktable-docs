.. _tracktable_api_label:

API Reference Documentation
===========================

The documentation in the section has been autogenerated from
the Python and C++ internal documentation describing algorithms, functions,
classes, parameters, inputs and outputs.

The Python and C++ interfaces share the same functionality, but they are
accessed through different interfaces. We prefer to implement things in Python first for
ease, development speed and malleability, then choose certain components to re-implement
in C++ based on runtime speed, memory usage and algorithmic needs.
However, there do exist C++ modules that have been Python wrapped so they can be
utilized directly in the Python interface to achieve the maximum performance out of the given algorithms.
These Python wrapped C++ algorithms are further described under the ``tracktable.lib module`` documentation.


Python API
----------

The Python interface is the primary way to access and utilize Tracktable's functions. This
interface provides the same access to functionality as you would find if you were directly
accessing the C++ interface. This includes functionality to read, write, create,
modify and analyze trajectories and points as well as rendering movies and images. Detailed
information about each of the operations listed above and information about the specifics about
points and trajectories can be found in the modules listed below.

.. note:: There may be functionality available in the Python interface that is unavailable in the C++ interface.

.. toctree::
   :maxdepth: 5

   python/tracktable.algorithms.rst
   python/tracktable.analysis.rst
   python/tracktable.applications.rst
   python/tracktable.core.rst
   python/tracktable.data_generators.rst
   python/tracktable.domain.rst
   python/tracktable.examples.rst
   python/tracktable.feature.rst
   python/tracktable.filter.rst
   python/tracktable.info.rst
   python/tracktable.rw.rst
   python/tracktable.lib.rst
   python/tracktable.render.rst
   python/tracktable.script_helpers.rst


C++ API
-------

The C++ interface provides access to all of the core components of the
Tracktable library. This includes functionality to read, write, create,
modify and analyze trajectories and points as well as rendering movies and images.
Detailed information about each of the operations listed above and information about the specifics about
points and trajectories can be found in the modules listed below.

.. note:: There may be functionality available in the C++ interface that is unavailable in the Python interface.

.. toctree::
   :maxdepth: 5

   cpp/tracktable.analysis.rst
   cpp/tracktable.core.rst
   cpp/tracktable.data_generators.rst
   cpp/tracktable.domain.rst
   cpp/tracktable.rw.rst
   cpp/tracktable.namespaces.rst
