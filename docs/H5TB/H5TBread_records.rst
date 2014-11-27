H5TBread_records
^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBread_records ( hid_t loc_id, const char *table_name,\
		hsize_t start, hsize_t nrecords, size_t type_size,  \
		const size_t *field_offset, const size_t *dst_sizes, \
		void *data )
   
   ``H5TBread_records`` reads some records identified from a dataset named
   ``table_name`` attached to the object specified by the identifier ``loc_id``.
		
   :synopsis: Reads records.

   :param loc_id: IN: Identifier of the file or group to read the table within.
   :param table_name IN: The name of the dataset to read.
   :param start: IN: The start record to read from.
   :param nrecords: IN: The number of records to read.
   :param type_size: IN: The size of the structure type, as calculated by \
		     ``sizeof()``.
   :param field_offset: IN: An array containing the offsets of the fields. \
			These offsets can be calculated with the ``HOFFSET`` \
			macro.
   :param dst_sizes: IN: An array containing the size in bytes of the fields.
   :param data: OUT: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
