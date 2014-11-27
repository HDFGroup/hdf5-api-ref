H5TBwrite_fields_index
^^^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBwrite_fields_index(hid_t loc_id, \
		const char *table_name, int nfields, const int *field_index, \
		hsize_t start, hsize_t nrecords, size_t type_size, \
		const size_t *field_offset, const size_t* field_sizes, \
		const void *data )

   ``H5TBwrite_fields_index`` overwrites one or several fields contained in
   the buffer ``field_index`` from a dataset named ``table_name`` attached to
   the object specified by the identifier ``loc_id``. 

   :synopsis: Overwrites fields.
   
   :param loc_id: IN: Identifier of the file or group where the table is \
		  located.
   :param table_name: IN: The name of the dataset to overwrite.
   :param nfields: IN: The number of fields to overwrite. This parameter is \
		   also the size of the ``field_index`` array.
   :param field_index: IN: The indexes of the fields to write.
   :param start: IN: The zero based index record to start writing.
   :param nrecords: IN: The number of records to write.
   :param type_size: IN: The size of the structure type, as calculated by \
		     ``sizeof()``.
   :param field_offset: IN: An array containing the offsets of the fields. \
			These offsets can be calculated with the ``HOFFSET``
			macro.
   :param field_sizes: IN: An array containing the sizes of the fields.
   :param data: IN: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

.. _h5tbwrite_field_index_f:

:strong:`Fortran90 Interface:` ``h5tbwrite_field_index_f``

.. code-block:: fortran

   subroutine h5tbwrite_field_index_f(loc_id, dset_name, field_index, start, &
                                      nrecords, type_size, buf, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id           ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name      ! name of the dataset 
     integer, intent(IN) :: field_index             ! index
     integer(HSIZE_T), intent(IN) :: start          ! start record 
     integer(HSIZE_T), intent(IN) :: nrecords       ! records
     integer(SIZE_T), intent(IN) :: type_size       ! type size
     <TYPE>, intent(IN), dimension(*) :: buf        ! data buffer 
     integer :: errcode                             ! error code
   end subroutine h5tbwrite_field_index_f
