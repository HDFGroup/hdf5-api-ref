
H5IMis_palette
^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMis_palette(hid_t loc_id, const char *dset_name)

   ``H5IMis_palette`` inquires if a dataset named ``dset_name``, attached to
   the file or group specified by the identifier ``loc_id``, is a palette
   based on the HDF5 Image and Palette Specification.

   :synopsis: Inquires if a dataset is a palette.
   
   :param loc_id: IN: Identifier of the file or group in which the image \
		  dataset is located.
   :param dataset_name: IN: The name of the dataset.
   :return: Returns true, false, fail.

.. _h5imis_palette_f:

:strong:`Fortran90 Interface:` ``h5imis_palette_f``

.. code-block:: fortran

   integer function h5imis_palette_f(loc_id, dset_name)
     implicit none
     integer(HID_T), intent(IN) :: loc_id         ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name    ! name of the dataset 
     integer :: errcode                           ! error code
   end function h5imis_palette_f
