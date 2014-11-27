H5TBwrite_fields_name
^^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBwrite_fields_name(hid_t loc_id, \
		const char *table_name, const char *field_names, hsize_t start,\
		hsize_t nrecords, size_t type_size, const size_t *field_offset,\
		const size_t *field_sizes, const void *data )

   ``H5TBwrite_fields_name`` overwrites one or several fields contained in the
   buffer ``field_names`` from a dataset named ``table_name`` attached to the
   object specified by the identifier ``loc_id``. 

   :synopsis: Overwrites fields.
   
   :param loc_id: IN: Identifier of the file or group where the table is \
		  located.
   :param table_name: IN: The name of the dataset to overwrite.
   :param field_names: IN: The names of the fields to write.
   :param start: IN: The zero based index record to start writing.
   :param nrecords: IN: The number of records to write.
   :param type_size: IN: The size of the structure type, as calculated by \
		     ``sizeof()``.
   :param field_offset: IN: An array containing the offsets of the fields. \
			These offsets can be calculated with the ``HOFFSET``\
			macro.
   :param field_sizes: IN: An array containing the sizes of the fields.
   :param data: IN: Buffer with data.      
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

.. _h5tbwrite_field_name_f:

:strong:`Fortran90 Interface:` ``h5tbwrite_field_name_f``

.. code-block:: fortran

   subroutine h5tbwrite_field_name_f(loc_id, dset_name, field_name, start, &
                                     nrecords, type_size, buf, errcode) 

     implicit none
     integer(HID_T), intent(IN) :: loc_id           ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name      ! name of the dataset 
     character(LEN=*), intent(IN) :: field_name     ! name of the field
     integer(HSIZE_T), intent(IN) :: start          ! start record 
     integer(HSIZE_T), intent(IN) :: nrecords       ! records
     integer(SIZE_T), intent(IN) :: type_size       ! type size
     <TYPE>, intent(IN), dimension(*) :: buf        ! data buffer 
     integer :: errcode                             ! error code

     end subroutine h5tbwrite_field_name_f
