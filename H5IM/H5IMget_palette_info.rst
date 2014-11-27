
H5IMget_palette_info
^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMget_palette_info(hid_t loc_id, const char *image_name, int pal_number, hsize_t *pal_dims)

   ``H5IMget_palette_info`` gets the dimensions of the palette dataset
   identified by ``pal_number`` (a zero based index) associated to an image
   specified by ``image_name``.

   :synopsis: Gets information about a palette dataset (dimensions).
   
   :param loc_id: IN: Identifier of the file or group in which the image dataset is located.
   :param image_name: IN: The name of the image dataset.
   :param pal_number: IN: The zero based index that identifies the palette.
   :param pal_dims: OUT: The dimensions of the palette dataset.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
