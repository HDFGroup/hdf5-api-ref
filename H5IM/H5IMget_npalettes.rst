
H5IMget_npalettes
^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMget_npalettes(hid_t loc_id, const char *image_name, hssize_t *npals)

   ``H5IMget_npalettes`` gets the number of palettes associated to an image
   specified by ``image_name``.

   :synopsis: Gets the number of palettes associated to an image.
   
   :param loc_id: IN: Identifier of the file or group in which the image dataset is located.
   :param image_name: IN: The name of the image dataset.
   :param npals: OUT: The number of palettes.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
