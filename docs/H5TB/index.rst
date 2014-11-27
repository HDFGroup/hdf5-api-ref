
HDF5 Table (H5TB)
-----------------

The HDF5 Table API defines a standard storage for HDF5 datasets that are
indented to be interpreted as tables. A table is defined as a collection of
records whose values are stored in fixed-length fields. All records have the
same structure and all values in each field have the same data type. 

The following functions are part of the HDF5 Table API. 

:strong:`Programming Hints:`

To use any of these functions or subroutines, you must first include the
relevant include file (C) or module (Fortran) in your application.

The following line includes the HDF5 Table package, ``H5TB``, in C applications:

.. code-block:: c
   
   #include "hdf5_hl.h"

This line includes the ``H5TB`` module in Fortran applications:

.. code-block:: fortran
   
   use h5tb

Creation
^^^^^^^^

.. toctree::
   :maxdepth: 2

   H5TBmake_table

Storage
^^^^^^^

.. toctree::
   :maxdepth: 2

   H5TBappend_records
   H5TBwrite_records
   H5TBwrite_fields_name
   H5TBwrite_fields_index
