H5TBdelete_field
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBdelete_field ( hid_t loc_id, const char *dset_name,\
		const char *field_name )
   
   ``H5TBdelete_field deletes`` a field named ``field_name`` from the table
   ``dset_name``. Note: this function requires the table to be re-created and
   rewritten in its entirety, and this can result in some unused space in the
   file, and can also take a great deal of time if the table is large.
		
   :synopsis: Deletes a field from a table.

   :param loc_id: IN: Identifier of the file or group in which the table is \
		  located.
   :param dset_name: IN: The name of the table.
   :param field_name: IN: The name of the field to delete.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

 .. _h5tbdelete_field_f:

:strong:`Fortran90 Interface:` ``h5tbdelete_field_f``

.. code-block:: fortran

   subroutine h5tbdelete_field_f(loc_id, dset_name, field_name, errcode)
     implicit none
     integer(HID_T), intent(IN) :: loc_id        ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name   ! name of the dataset 
     character(LEN=*), intent(IN) :: field_name  ! name of the field
     integer :: errcode                          ! error code
   end subroutine h5tbdelete_field_f
