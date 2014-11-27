H5TBadd_records_from
^^^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBadd_records_from ( hid_t loc_id, \
		const char *dset_name1, hsize_t start1, hsize_t nrecords, \
		const char *dset_name2, hsize_t start2 )
   
   ``H5TBadd_records_from`` adds records from a dataset named ``dset_name1`` \
   to a dataset named ``dset_name2``. Both tables are attached to the object
   specified by the identifier ``loc_id``. 
		
   :synopsis: Add records from first table to second table.
   
   :param loc_id: IN: Identifier of the file or group in which the table is \
		  located.
   :param dset_name1: IN: The name of the dataset to read the records.
   :param start1: IN: The position to read the records from the first table
   :param nrecords: IN: The number of records to read from the first table.
   :param dset_name2: IN: The name of the dataset to write the records.
   :param start2: IN: The position to write the records on the second table
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
