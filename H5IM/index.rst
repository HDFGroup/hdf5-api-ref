
HDF5 Image (H5IM)
-----------------

The HDF5 Image API defines a standard storage for HDF5 datasets that are
indented to be interpreted as images. The specification for this API is
presented in another document: `HDF5 Image and Palette Specification
<http://www.hdfgroup.org/HDF5/doc/ADGuide/ImageSpec.html>`_.
This version of the API is primarily concerned with two dimensional raster
data similar to HDF4 Raster Images. The HDF5 image API uses the `Lite HDF5 API
<http://www.hdfgroup.org/HDF5/doc/HL/RM_H5LT.html>`_.

The following functions are part of the HDF5 Image API version 1.0.

:strong:`Programming Hints:`

To use any of these functions or subroutines, you must first include the
relevant include file (C) or module (Fortran) in your application.

The following line includes the HDF5 Image package, ``H5IM``, in C applications:

.. code-block:: c
   
   #include "hdf5_hl.h"

This line includes the ``H5IM`` module in Fortran applications:

.. code-block:: fortran
   
   use h5im

Image Functions
^^^^^^^^^^^^^^^

.. toctree::
   :maxdepth: 2

   H5IMget_image_info
   H5IMis_image
   H5IMmake_image_8bit
   H5IMmake_image_24bit
   H5IMread_image

Palette Functions
^^^^^^^^^^^^^^^^^
		
.. toctree::
   :maxdepth: 2

   H5IMget_npalettes
   H5IMget_palette
   H5IMget_palette_info
   H5IMis_palette
   H5IMlink_palette
   H5IMmake_palette
   H5IMunlink_palette
