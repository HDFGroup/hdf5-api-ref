H5TBget_field_info
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBget_field_info ( hid_t loc_id, \
		const char *table_name, char *field_names[], \
		size_t *field_sizes, size_t *field_offsets, size_t *type_size  )
		
   ``H5TBget_field_info`` gets information about a dataset named ``table_name``
   attached to the object specified by the identifier ``loc_id``. 
		
   :synopsis: Gets information about a table.

   :param loc_id: IN: Identifier of the file or group to read the table within.
   :param table_name: IN: The name of the dataset to read.
   :param field_names: OUT: An array containing the names of the fields.
   :param field_sizes: OUT: An array containing the size of the fields.
   :param field_offsets: OUT: An array containing the offsets of the fields.
   :param type_size: OUT: The size of the HDF5 datatype associated with the \
		     table. More specifically, the size in bytes of the HDF5 \
		     compound datatype used to define a row, or record, in the\
		     table.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

 .. _h5tbget_field_info_f:

:strong:`Fortran90 Interface:` ``h5tbget_field_info_f``

.. code-block:: fortran

   subroutine h5tbget_field_info_f(loc_id, dset_name, nfields, field_names, & 
                                   field_sizes, field_offsets, type_size, & 
                                   errcode, maxlen_out)
     implicit none
     integer(HID_T), intent(IN) :: loc_id         ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name    ! name of the dataset 
     integer(HSIZE_T), intent(IN):: nfields       ! nfields 
     character(LEN=*), dimension(nfields), intent(INOUT) :: field_names    
                                                  ! field names
     integer(SIZE_T), dimension(nfields), intent(INOUT) :: field_sizes    
                                                  ! field sizes
     integer(SIZE_T), dimension(nfields), intent(INOUT) :: field_offsets  
                                                  ! field offsets
     integer(SIZE_T), intent(INOUT):: type_size   ! type size 
     integer :: errcode                           ! error code
     integer, optional :: maxlen_out              ! returns maximum character 
                                                  ! length of field_names
   end subroutine h5tbget_field_info_f
