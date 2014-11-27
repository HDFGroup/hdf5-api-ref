
H5IMis_palette
^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMis_palette(hid_t loc_id, const char *dset_name)

   ``H5IMis_palette`` inquires if a dataset named ``dset_name``, attached to
   the file or group specified by the identifier ``loc_id``, is a palette
   based on the HDF5 Image and Palette Specification.

   :synopsis: Inquires if a dataset is a palette.
   
   :param loc_id: IN: Identifier of the file or group in which the image dataset is located.
   :param dataset_name: IN: The name of the dataset.
   :return: Returns true, false, fail.
