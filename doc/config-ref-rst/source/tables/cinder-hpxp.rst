..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _cinder-hpxp:

.. list-table:: Description of HP XP volume driver configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``hpxp_async_copy_check_interval`` = ``10``
     - (IntOpt) Interval to check copy asynchronously
   * - ``hpxp_compute_target_ports`` = ``None``
     - (ListOpt) Target port names of compute node for host group or iSCSI target
   * - ``hpxp_copy_check_interval`` = ``3``
     - (IntOpt) Interval to check copy
   * - ``hpxp_copy_speed`` = ``3``
     - (IntOpt) Copy speed of storage system
   * - ``hpxp_default_copy_method`` = ``FULL``
     - (StrOpt) Default copy method of storage system. There are two valid values: "FULL" specifies that a full copy; "THIN" specifies that a thin copy. Default value is "FULL"
   * - ``hpxp_group_request`` = ``False``
     - (BoolOpt) Request for creating host group or iSCSI target
   * - ``hpxp_horcm_add_conf`` = ``True``
     - (BoolOpt) Add to HORCM configuration
   * - ``hpxp_horcm_name_only_discovery`` = ``False``
     - (BoolOpt) Only discover a specific name of host group or iSCSI target
   * - ``hpxp_horcm_numbers`` = ``200, 201``
     - (ListOpt) Instance numbers for HORCM
   * - ``hpxp_horcm_resource_name`` = ``meta_resource``
     - (StrOpt) Resource group name of storage system for HORCM
   * - ``hpxp_horcm_user`` = ``None``
     - (StrOpt) Username of storage system for HORCM
   * - ``hpxp_ldev_range`` = ``None``
     - (StrOpt) Logical device range of storage system
   * - ``hpxp_pool`` = ``None``
     - (StrOpt) Pool of storage system
   * - ``hpxp_storage_cli`` = ``None``
     - (StrOpt) Type of storage command line interface
   * - ``hpxp_storage_id`` = ``None``
     - (StrOpt) ID of storage system
   * - ``hpxp_target_ports`` = ``None``
     - (ListOpt) Target port names for host group or iSCSI target
   * - ``hpxp_thin_pool`` = ``None``
     - (StrOpt) Thin pool of storage system
   * - ``hpxp_zoning_request`` = ``False``
     - (BoolOpt) Request for FC Zone creating host group
