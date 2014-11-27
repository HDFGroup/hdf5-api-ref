
H5IMunlink_palette
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMunlink_palette( hid_t loc_id, const char *image_name, const char *pal_name )

   ``H5IMunlink_palette`` detaches a palette from an image specified by
   ``image_name``.

   :synopsis: Detaches a palette from an image.
   
   :param loc_id: IN: Identifier of the file or group.
   :param image_name: IN: The name of the image dataset.
   :param pal_name: IN: The name of the palette.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
