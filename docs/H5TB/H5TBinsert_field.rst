H5TBinsert_field
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBinsert_field ( hid_t loc_id, const char *dset_name,\
		const char *field_name,  hid_t field_type, hsize_t position, \
		const void *fill_data, const void *data )
   
   ``H5TBinsert_field`` inserts a new field named ``field_name`` into the table
   ``dset_name``. Note: this function requires the table to be re-created and
   rewritten in its entirety, and this can result in some unused space in the
   file, and can also take a great deal of time if the table is large. 
		
   :synopsis: Insert a new field into a table.

   :param loc_id: IN: Identifier of the file or group in which the table is \
		  located.
   :param dset_name: IN: The name of the table.
   :param field_name: IN: The name of the field to insert.
   :param field_type: IN: The data type of the field.
   :param position: IN: The zero based index position where to insert the field.
   :param fill_data: IN: Fill value data for the field. This parameter can be \
		     ``NULL``.
   :param data: IN: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

 .. _h5tbinsert_field_f:

:strong:`Fortran90 Interface:` ``h5tbinsert_field_f``

.. code-block:: fortran

   subroutine h5tbinsert_field_f(loc_id, dset_name, field_name, field_type, &
                                 field_index, buf, errcode )
     implicit none
     integer(HID_T), intent(IN) :: loc_id           ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name      ! name of the dataset 
     character(LEN=*), intent(IN) :: field_name     ! name of the field
     integer(HID_T), intent(IN)   :: field_type     ! field type
     integer, intent(IN) :: field_index             ! field_index
     <TYPE>, intent(IN), dimension(*) :: buf        ! data buffer 
     integer :: errcode                             ! error code
   end subroutine h5tbinsert_field_f
