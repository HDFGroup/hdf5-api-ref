
H5IMmake_image_8bit
^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMmake_image_8bit(hid_t loc_id, const char *dset_name, hsize_t width, hsize_t height, const unsigned char *buffer)

   ``H5IMmake_image_8bit`` creates and writes a dataset named ``dset_name``
   attached to the file or group specified by the identifier ``loc_id``.
   Attributes conforming to the HDF5 Image and Palette specification for an
   indexed image are attached to the dataset, thus identifying it as an image.
   The image data is of the type ``H5T_NATIVE_UCHAR``. An indexed image is an
   image in which each each pixel information storage is an index to a table
   palette.

   :synopsis: Creates and writes an image.
   
   :param loc_id: IN: Identifier of the file or group to create the dataset within.
   :param dset_name: IN: The name of the dataset to create.
   :param width: IN: The width of the image.
   :param height: IN: The height of the image.
   :param buffer: IN: Buffer with data to be written to the dataset.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
