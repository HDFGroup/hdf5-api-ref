
H5IMget_image_info
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMget_image_info( hid_t loc_id, \
   const char *dset_name,  hsize_t *width, hsize_t *height, hsize_t *planes, \
   char *interlace, hssize_t *npals)

   ``H5IMget_image_info`` gets information about an image named ``dset_name``
   attached to the file or group specified by the identifier ``loc_id``.

   :synopsis: Gets information about an image dataset (dimensions, interlace \
	      mode and number of associated palettes).
   
   :param loc_id: IN: Identifier of the file or group in which the dataset \
		  is located.
   :param dset_name: IN: The name of the dataset.
   :param width: OUT: The width of the image.
   :param height: OUT: The height of the image.
   :param planes: OUT: The number of color planes of the image.
   :param interlace: OUT: The interlace mode of the image.
   :param npals: OUT: The number of palettes associated to the image.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

.. _h5imget_image_info_f:

:strong:`Fortran90 Interface:` ``h5imget_image_info_f``

.. code-block:: fortran

   subroutine h5imget_image_info_f(loc_id, dset_name, width, height, planes, &
                                   interlace, npals, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id            ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name       ! name of the dataset 
     integer(HSIZE_T), intent(INOUT) :: width        ! width of image  
     integer(HSIZE_T), intent(INOUT) :: height       ! height of image
     integer(HSIZE_T), intent(INOUT) :: planes       ! color planes
     integer(HSIZE_T), intent(INOUT) :: npals        ! palettes
     character(LEN=*), intent(INOUT) :: interlace    ! interlace 
     integer :: errcode                              ! error code
   end subroutine h5imget_image_info_f   
