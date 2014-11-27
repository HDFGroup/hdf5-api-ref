H5TBget_table_info
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBget_table_info ( hid_t loc_id, \
		const char *table_name, hsize_t *nfields, hsize_t *nrecords )
		
   ``H5TBget_dimensions`` retrieves the table dimensions from a dataset named
   ``table_name`` attached to the object specified by the identifier
   ``loc_id``. 
		
   :synopsis: Gets the table dimensions.

   :param loc_id: IN: Identifier of the file or group to read the table within.
   :param table_name: IN: The name of the dataset to read.
   :param nfields: OUT: The number of fields.
   :param nrecords: OUT: The number of records.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.

 .. _h5tbget_table_info_f:

:strong:`Fortran90 Interface:` ``h5tbget_table_info_f``

.. code-block:: fortran

   subroutine h5tbget_table_info_f(loc_id, dset_name, nfields, nrecords, errcode) 

     implicit none
     integer(HID_T), intent(IN) :: loc_id        ! file or group identifier 
     character(LEN=*), intent(IN) :: dset_name   ! name of the dataset 
     integer(HSIZE_T), intent(INOUT):: nfields   ! nfields 
     integer(HSIZE_T), intent(INOUT):: nrecords  ! nrecords 
     integer :: errcode                          ! error code
   end subroutine h5tbget_table_info_f
