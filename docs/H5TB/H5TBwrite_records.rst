H5TBwrite_records
^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBwrite_records(hid_t loc_id, const char *table_name,\
		hsize_t start, hsize_t nrecords, size_t type_size, \
		const size_t *field_offset, const size_t *field_sizes, \
		const void *data)
   
   ``H5TBwrite_records`` overwrites records starting at the zero index position
   start of the table named ``table_name`` attached to the object specified by
   the identifier ``loc_id``.

   :synopsis: Overwrites records.
   
   :param loc_id: IN: Identifier of the file or group where the table is \
		  located.
   :param table_name: IN: The name of the dataset to overwrite.
   :param start: IN: The zero index record to start writing. 
   :param nrecords: IN: The number of records to write.
   :param type_size: IN: The size of the structure type, as calculated by \
		     ``sizeof()``.
   :param field_offset: IN: An array containing the offsets of the fields. \
			These offsets can be calculated with the ``HOFFSET`` \
			macro.
   :param field_sizes: IN: An array containing the sizes of the fields.
   :param data: IN: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
