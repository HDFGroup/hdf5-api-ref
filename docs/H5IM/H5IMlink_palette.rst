
H5IMlink_palette
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMlink_palette( hid_t loc_id, const char *image_name, \
		const char *pal_name)

   ``H5IMlink_palette`` attaches a palette named ``pal_name`` to an image
   specified by ``image_name``. The image dataset may or not already have an
   attached palette. If it has, the array of palette references is extended to
   hold the reference to the new palette.

   :synopsis: Attaches a palette to an image.
   
   :param loc_id: IN: Identifier of the file or group.
   :param image_name: IN: The name of the dataset to attach the palette to.
   :param pal_name: IN: The name of the palette.
   :return: Returns a non-negative value if successful; otherwise returns a \
	    negative value.

.. _h5imlink_palette_f:

:strong:`Fortran90 Interface:` ``h5imlink_palette_f``

.. code-block:: fortran

   subroutine h5imlink_palette_f(loc_id, dset_name, pal_name, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id          ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name     ! name of the dataset 
     character(LEN=*), intent(IN) :: pal_name      ! palette name 
     integer :: errcode                            ! error code 
   end subroutine h5imlink_palette_f
