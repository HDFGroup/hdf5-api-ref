
H5IMis_image
^^^^^^^^^^^^

.. c:function:: herr_t H5IMis_image ( hid_t loc_id, const char *dset_name )

   ``H5IMis_image`` inquires if a dataset named ``dset_name``, attached to
   the file or group specified by the identifier ``loc_id``, is an image based
   on the HDF5 Image and Palette Specification.

   :synopsis: Inquires if a dataset is an image.
   
   :param loc_id: IN: Identifier of the file or group in which the dataset is located.
   :param dset_name: IN: The name of the dataset.
   :return: Returns true, false, fail.
