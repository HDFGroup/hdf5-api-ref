H5TBread_fields_name
^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBread_fields_name ( hid_t loc_id, \
		const char *table_name, const char * field_names, \
		hsize_t start, hsize_t nrecords, size_t type_size, \
		const size_t *field_offset, const size_t *dst_sizes, void *data)
		
   ``H5TBread_fields_name`` reads the fields identified by ``field_names`` from
   a dataset named ``table_name`` attached to the object specified by the
   identifier ``loc_id``. 
		
   :synopsis: Reads one or several fields. The fields are identified by name.

   :param loc_id: IN: Identifier of the file or group to read the table within.
   :param table_name: IN: The name of the dataset to read.
   :param field_names: IN: An array containing the names of the fields to read.
   :param start: IN: The start record to read from.
   :param nrecords: IN: The number of records to read.
   :param type_size: IN: The size in bytes of the structure associated with \
		     the table. This value is obtained with ``sizeof``.
   :param field_offset: IN: An array containing the offsets of the fields.
   :param dst_sizes: IN: An array containing the size in bytes of the fields.
   :param data: OUT: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

 .. _h5tbread_field_name_f:

:strong:`Fortran90 Interface:` ``h5tbread_field_name_f``

.. code-block:: fortran

   subroutine h5tbread_field_name_f(loc_id, dset_name, field_name, start, &
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
   end subroutine h5tbread_field_name_f
