
H5IMlink_palette
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMlink_palette( hid_t loc_id, const char *image_name, const char *pal_name)

   ``H5IMlink_palette`` attaches a palette named ``pal_name`` to an image
   specified by ``image_name``. The image dataset may or not already have an
   attached palette. If it has, the array of palette references is extended to
   hold the reference to the new palette.

   :synopsis: Attaches a palette to an image.
   
   :param loc_id: IN: Identifier of the file or group.
   :param image_name: IN: The name of the dataset to attach the palette to.
   :param pal_name: IN: The name of the palette.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
