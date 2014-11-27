H5TBappend_records
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBappend_records(hid_t loc_id, const char *dset_name,\
		hsize_t nrecords, size_t type_size, const size_t *field_offset,\
		const size_t *field_sizes, const void *data )

   ``H5TBappend_records`` adds records to the end of the table named
   ``dset_name`` attached to the object specified by the identifier ``loc_id``.
   The dataset is extended to hold the new records.   

   :synopsis: Adds records to the end of the table.
   
   :param loc_id: IN: Identifier of the file or group where the table is \
		  located.
   :param dset_name: IN: The name of the dataset to overwrite.
   :param nrecords: IN: The number of records to append.
   :param type_size: IN: The size of the structure type, as calculated by \
		     ``sizeof()``.
   :param field_offset: IN: An array containing the offsets of the fields. \
			These offsets can be calculated with the ``HOFFSET`` \
			macro.
   :param field_sizes: IN: An array containing the sizes of the fields.
   :param data: IN: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
