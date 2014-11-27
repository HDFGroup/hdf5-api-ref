
H5IMmake_image_8bit
^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMmake_image_8bit(hid_t loc_id, \
		const char *dset_name, hsize_t width, hsize_t height, \
		const unsigned char *buffer)

   ``H5IMmake_image_8bit`` creates and writes a dataset named ``dset_name``
   attached to the file or group specified by the identifier ``loc_id``.
   Attributes conforming to the HDF5 Image and Palette specification for an
   indexed image are attached to the dataset, thus identifying it as an image.
   The image data is of the type ``H5T_NATIVE_UCHAR``. An indexed image is an
   image in which each each pixel information storage is an index to a table
   palette.

   :synopsis: Creates and writes an image.
   
   :param loc_id: IN: Identifier of the file or group to create the dataset \
		  within.
   :param dset_name: IN: The name of the dataset to create.
   :param width: IN: The width of the image.
   :param height: IN: The height of the image.
   :param buffer: IN: Buffer with data to be written to the dataset.
   :return: Returns a non-negative value if successful; otherwise returns a \
	    negative value.

.. _h5immake_image_8bit_f:

:strong:`Fortran90 Interface:` ``h5immake_image_8bit_f``

.. code-block:: fortran
   
   subroutine h5immake_image_8bit_f(loc_id, dset_name, width, height, buf, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id           ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name      ! name of the dataset 
     integer(HSIZE_T), intent(IN) :: width          ! width of image  
     integer(HSIZE_T), intent(IN) :: height         ! height of image
     integer*1, intent(IN), dimension(*) :: buf     ! 1 byte integer data buffer 
     integer :: errcode                             ! error code
   end subroutine h5immake_image_8bit_f
