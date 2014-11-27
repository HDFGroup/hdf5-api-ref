H5TBread_table
^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBread_table( hid_t loc_id, const char *table_name, \
		size_t dst_size,  const size_t *dst_offset, \
		const size_t *dst_sizes, void *dst_buf )
   
   ``H5TBread_table`` reads a table named ``table_name` attached to the object
   specified by the identifier ``loc_id``. 
		
   :synopsis: Reads a table.

   :param loc_id: IN: Identifier of the file or group to read the table within.
   :param table_name: IN: The name of the dataset to read.
   :param dst_size: IN: The size of the structure type, as calculated by \
		    ``sizeof()``.
   :param dst_offset: IN: An array containing the offsets of the fields. \
		      These offsets can be calculated with the ``HOFFSET`` \
		      macro.
   :param dst_sizes: IN: An array containing the sizes of the fields. These \
		     sizes can be calculated with the ``sizeof()`` macro.
   :param dst_buf: OUT: Buffer with data.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
