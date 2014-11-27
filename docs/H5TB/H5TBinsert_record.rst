H5TBinsert_record
^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBinsert_record (hid_t loc_id, const char *dset_name,\
		hsize_t start, hsize_t nrecords, size_t type_size,  \
		const size_t *field_offset, void *data  )
   
   ``H5TBinsert_record`` inserts records into the middle of the table
   ("pushing down" all the records after it)
		
   :synopsis: Insert records.
   
   :param loc_id: IN: Identifier of the file or group in which the table is \
		  located.
   :param dset_name: IN: The name of the dataset.
   :param start: IN: The position to insert.
   :param nrecords: IN: The number of records to insert.
   :param data: IN: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
