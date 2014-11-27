
H5IMread_image
^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMread_image ( hid_t loc_id, const char *dset_name, unsigned char *buffer )

   ``H5IMread_image`` reads a dataset named ``dset_name`` attached to the
   file or group specified by the identifier ``loc_id``.

   :synopsis: Reads image data from disk.
   
   :param loc_id: IN: Identifier of the file or group to read the dataset from.
   :param dset_name: IN: The name of the dataset.
   :param buffer: OUT: Buffer with data to store the image.
   :return: Returns a non-negative value if successful; otherwise returns a negative value.
