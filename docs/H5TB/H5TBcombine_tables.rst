H5TBcombine_tables
^^^^^^^^^^^^^^^^^^

.. c:function:: herr_t H5TBcombine_tables ( hid_t loc_id1, \
		const char *dset_name1, hid_t loc_id2, const char *dset_name2,\
		const char *dset_name3 )
   
   ``H5TBcombine_tables`` combines records from two datasets named
   ``dset_name1`` and ``dset_name2``, to a new table named ``dset_name3``.
   These tables can be located on different files, identified by ``loc_id1``
   and ``loc_id2`` (identifiers obtained with ``H5Fcreate``). They can also
   be located on the same file. In this case one uses the same identifier for
   both parameters ``loc_id1`` and ``loc_id2``. If two files are used, the
   third table is written on the first file.
		
   :synopsis: Combines records from two tables into a third.

   :param loc_id1: IN: Identifier of the file or group in which the first \
		   table is located.
   :param dset_name1: IN: The name of the first table to combine.
   :param loc_id2: IN: Identifier of the file or group in which the second \
		   table is located.
   :param dset_name2: IN: The name of the second table to combine.
   :param dset_name3: IN: The name of the new table.
   :return: Returns a non-negative value if successful; otherwise returns \
	    a negative value.
