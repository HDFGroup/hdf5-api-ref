
H5IMmake_palette
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMmake_palette(hid_t loc_id, const char *pal_name, \
		const hsize_t *pal_dims, const unsigned char *pal_data)

   ``H5IMmake_palette`` creates and writes a dataset named ``pal_name``.
   Attributes conforming to the HDF5 Image and Palette specification are
   attached to the dataset, thus identifying it as a palette. The palette
   data is of the type ``H5T_NATIVE_UCHAR``.

   :synopsis: Creates and writes a palette.
   
   :param loc_id: IN: Identifier of the file or group to create the dataset \
		  within.
   :param pal_name: IN: The name of the palette.
   :param pal_dims: IN: An array of the size of the palette dimensions.
   :param pal_data: IN: Buffer with data to be written to the dataset.
   :return: Returns a non-negative value if successful; otherwise returns a \
	    negative value.

.. _h5immake_palette_f:

:strong:`Fortran90 Interface:` ``h5immake_palette_f``

.. code-block:: fortran
   
   subroutine h5immake_palette_f(loc_id, dset_name, pal_dims, buf, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id           ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name      ! name of the dataset 
     integer(HSIZE_T), intent(IN), dimension(*) :: pal_dims 
		                                    ! dimensions  
     integer*1, intent(IN), dimension(*) :: buf     ! 1 byte integer data buffer
     integer :: errcode                             ! error code
   end subroutine h5immake_palette_f
