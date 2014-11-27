H5TBmake_table
^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBmake_table( const char *table_title, hid_t loc_id,\
		const char *dset_name, hsize_t nfields, const hsize_t nrecords,\
		size_t type_size, const char *field_names [ ], \
		const size_t *field_offset, const hid_t *field_types, \
		hsize_t chunk_size, void *fill_data, int compress, \
		const void *data )

   ``H5TBmake_table creates`` and writes a dataset named ``table_name``
   attached to the object specified by the identifier ``loc_id``.

   :synopsis: Creates and writes a table.
   
   :param loc_id: IN: Identifier of the file or group in which the dataset \
		  is located.
   :param table_title: IN: The title of the table.
   :param loc_id: IN: Identifier of the file or group to create the table \
		  within.
   :param table_name: IN: The name of the dataset to create.
   :param nfields: IN: The number of fields.
   :param nrecords: IN: The number of records.
   :param type_size: IN: The size in bytes of the structure associated with \
		     the table. This value is obtained with ``sizeof``.
   :param field_names: IN: An array containing the names of the fields.
   :param field_offset: IN: An array containing the offsets of the fields.
   :param field_types: IN: An array containing the type of the fields.
   :param chunk_size: IN: The chunk size.
   :param fill_data: IN: Fill values data.
   :param compress: IN: Flag that turns compression on or off.
   :param data:	IN: Buffer with data to be written to the table.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

.. _h5tbmake_table_f:

:strong:`Fortran90 Interface:` ``h5tbmake_table_f``

.. note::
   ``h5tbmake_table_f`` only creates the table, it does not write data to it.
   
.. code-block:: fortran

   subroutine h5tbmake_table_f(table_title, loc_id, dset_name, nfields, &
		               nrecords, type_size, field_names, field_offset, &
                               field_types, chunk_size, compress, errcode) 
     implicit none
     character(LEN=*), intent(IN) :: table_title     ! name of the table
     integer(HID_T), intent(IN) :: loc_id            ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name       ! name of the dataset 
     integer(HSIZE_T), intent(IN) :: nfields         ! fields 
     integer(HSIZE_T), intent(IN) :: nrecords        ! records
     integer(SIZE_T), intent(IN) :: type_size        ! type size
     character(LEN=*), dimension(nfields), intent(IN) :: field_names
                                                     ! field names
     integer(SIZE_T), dimension(nfields), intent(IN) :: field_offset
                                                     ! field offset
     integer(HID_T), dimension(nfields), intent(IN) :: field_types
                                                     ! field types
     integer(HSIZE_T), intent(IN) :: chunk_size      ! chunk size
     integer, intent(IN) :: compress                 ! compress
     integer :: errcode                              ! error code
   end subroutine h5tbmake_table_f
