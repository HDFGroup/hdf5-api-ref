H5TBdelete_record
^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBdelete_record ( hid_t loc_id, const char *dset_name,\
		hsize_t start, hsize_t nrecords )
   
   ``H5TBdelete_record`` deletes records from middle of table ("pulling up" \
   all the records after it)

   :synopsis: Delete records.
   
   :param loc_id: IN: Identifier of the file or group where the table is \
		  located.
   :param dset_name: IN: The name of the dataset.
   :param start: IN: The start record to delete from.
   :param nrecords: IN: The number of records to delete.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
