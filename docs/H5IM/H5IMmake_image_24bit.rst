
H5IMmake_image_24bit
^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5IMmake_image_24bit ( hid_t loc_id, \
		const char *dset_name,  hsize_t width, hsize_t height, \
		const char *interlace, const unsigned char *buffer)
   
   ``H5IMmake_image_24bit`` creates and writes a dataset named ``dset_name``
   attached to the file or group specified by the identifier ``loc_id``.
   This function defines a true color image conforming to the HDF5 Image and
   Palette specification. The function assumes that the image data is of the
   type ``H5T_NATIVE_UCHAR``.

   A true color image is an image where the pixel storage contains several
   color planes. In a 24 bit RGB color model, these planes are red, green and
   blue. In a true color image the stream of bytes can be stored in several
   different ways, thus defining the interlace (or interleaving) mode.
   The 2 most used types of interlace mode are interlace by pixel and
   interlace by plane. In the 24 bit RGB color model example, interlace by
   plane means all the red components for the entire dataset are stored first,
   followed by all the green components, and then by all the blue components.
   Interlace by pixel in this example means that for each pixel the sequence
   red, green, blue is defined. In this function, the interlace mode is defined
   in the parameter ``interlace``, a string that can have the values
   ``INTERLACE_PIXEL`` or ``INTERLACE_PLANE``.

   :synopsis: Creates and writes a true color image.
   
   :param loc_id: IN: Identifier of the file or group to create the dataset \
		  within.
   :param dset_name: IN: The name of the dataset to create.
   :param width: IN: The width of the image.
   :param height: IN: The height of the image.
   :param interlace: IN: String defining the interlace mode.
   :param buffer: IN: Buffer with data to be written to the dataset.
   :return: Returns a non-negative value if successful; otherwise returns a \
	    negative value.

.. _h5immake_image_24bit_f:

:strong:`Fortran90 Interface:` ``h5immake_image_24bit_f``

.. code-block:: fortran
   
   subroutine h5immake_image_24bit_f(loc_id, dset_name, width, height, il, &
                                     buf, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id         ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name    ! name of the dataset 
     integer(HSIZE_T), intent(IN) :: width        ! width of image  
     integer(HSIZE_T), intent(IN) :: height       ! height of image
     character(LEN=*), intent(IN) :: il           ! interlace
     integer*1, intent(IN), dimension(*) :: buf   ! 1 byte integer data buffer 
     integer :: errcode                           ! error code
   end subroutine h5immake_image_24bit_f
