
H5IMget_palette
^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMget_palette(hid_t loc_id, const char *image_name, \
		int pal_number, unsigned char *pal_data)

   ``H5IMget_palette`` gets the palette dataset identified by ``pal_number``
   (a zero based index) associated to an image specified by ``image_name``.

   :synopsis: Gets the palette dataset.
   
   :param loc_id: IN: Identifier of the file or group in which the image \
		  dataset is located.
   :param image_name: IN: The name of the image dataset.
   :param pal_number: IN: The zero based index that identifies the palette.
   :param pal_data: OUT: The palette dataset.
   :return: Returns a non-negative value if successful; otherwise returns a \
	    negative value.

.. _h5imget_palette_f:

:strong:`Fortran90 Interface:` ``h5imget_palette_f``

.. code-block:: fortran

   subroutine h5imget_palette_f(loc_id, dset_name, pal_number, buf, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id            ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name       ! name of the dataset 
     integer, intent(IN) :: pal_number               ! palette number
     integer*1, intent(INOUT), dimension(*) :: buf   ! 1 byte integer data buffer 
     integer :: errcode                              ! error code
   end subroutine h5imget_palette_f
