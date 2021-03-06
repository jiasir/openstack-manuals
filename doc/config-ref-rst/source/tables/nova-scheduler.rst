..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-scheduler:

.. list-table:: Description of scheduler configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``aggregate_image_properties_isolation_namespace`` = ``None``
     - (StrOpt) Force the filter to consider only keys matching the given namespace.
   * - ``aggregate_image_properties_isolation_separator`` = ``.``
     - (StrOpt) The separator used between the namespace and keys
   * - ``baremetal_scheduler_default_filters`` = ``RetryFilter, AvailabilityZoneFilter, ComputeFilter, ComputeCapabilitiesFilter, ImagePropertiesFilter, ExactRamFilter, ExactDiskFilter, ExactCoreFilter``
     - (ListOpt) Which filter class names to use for filtering baremetal hosts when not specified in the request.
   * - ``cpu_allocation_ratio`` = ``0.0``
     - (FloatOpt) Virtual CPU to physical CPU allocation ratio which affects all CPU filters. This configuration specifies a global ratio for CoreFilter. For AggregateCoreFilter, it will fall back to this configuration value if no per-aggregate setting found. NOTE: This can be set per-compute, or if set to 0.0, the value set on the scheduler node(s) will be used and defaulted to 16.0
   * - ``disk_allocation_ratio`` = ``1.0``
     - (FloatOpt) Virtual disk to physical disk allocation ratio
   * - ``io_ops_weight_multiplier`` = ``-1.0``
     - (FloatOpt) Multiplier used for weighing host io ops. Negative numbers mean a preference to choose light workload compute hosts.
   * - ``isolated_hosts`` =
     - (ListOpt) Host reserved for specific images
   * - ``isolated_images`` =
     - (ListOpt) Images to run on isolated host
   * - ``max_instances_per_host`` = ``50``
     - (IntOpt) Ignore hosts that have too many instances
   * - ``max_io_ops_per_host`` = ``8``
     - (IntOpt) Tells filters to ignore hosts that have this many or more instances currently in build, resize, snapshot, migrate, rescue or unshelve task states
   * - ``ram_allocation_ratio`` = ``0.0``
     - (FloatOpt) Virtual ram to physical ram allocation ratio which affects all ram filters. This configuration specifies a global ratio for RamFilter. For AggregateRamFilter, it will fall back to this configuration value if no per-aggregate setting found. NOTE: This can be set per-compute, or if set to 0.0, the value set on the scheduler node(s) will be used and defaulted to 1.5
   * - ``ram_weight_multiplier`` = ``1.0``
     - (FloatOpt) Multiplier used for weighing ram. Negative numbers mean to stack vs spread.
   * - ``reserved_host_disk_mb`` = ``0``
     - (IntOpt) Amount of disk in MB to reserve for the host
   * - ``reserved_host_memory_mb`` = ``512``
     - (IntOpt) Amount of memory in MB to reserve for the host
   * - ``restrict_isolated_hosts_to_isolated_images`` = ``True``
     - (BoolOpt) Whether to force isolated hosts to run only isolated images
   * - ``scheduler_available_filters`` = ``['nova.scheduler.filters.all_filters']``
     - (MultiStrOpt) Filter classes available to the scheduler which may be specified more than once. An entry of "nova.scheduler.filters.all_filters" maps to all filters included with nova.
   * - ``scheduler_default_filters`` = ``RetryFilter, AvailabilityZoneFilter, RamFilter, DiskFilter, ComputeFilter, ComputeCapabilitiesFilter, ImagePropertiesFilter, ServerGroupAntiAffinityFilter, ServerGroupAffinityFilter``
     - (ListOpt) Which filter class names to use for filtering hosts when not specified in the request.
   * - ``scheduler_driver`` = ``nova.scheduler.filter_scheduler.FilterScheduler``
     - (StrOpt) Default driver to use for the scheduler
   * - ``scheduler_driver_task_period`` = ``60``
     - (IntOpt) How often (in seconds) to run periodic tasks in the scheduler driver of your choice. Please note this is likely to interact with the value of service_down_time, but exactly how they interact will depend on your choice of scheduler driver.
   * - ``scheduler_host_manager`` = ``nova.scheduler.host_manager.HostManager``
     - (StrOpt) The scheduler host manager class to use
   * - ``scheduler_host_subset_size`` = ``1``
     - (IntOpt) New instances will be scheduled on a host chosen randomly from a subset of the N best hosts. This property defines the subset size that a host is chosen from. A value of 1 chooses the first host returned by the weighing functions. This value must be at least 1. Any value less than 1 will be ignored, and 1 will be used instead
   * - ``scheduler_instance_sync_interval`` = ``120``
     - (IntOpt) Waiting time interval (seconds) between sending the scheduler a list of current instance UUIDs to verify that its view of instances is in sync with nova. If the CONF option `scheduler_tracks_instance_changes` is False, changing this option will have no effect.
   * - ``scheduler_json_config_location`` =
     - (StrOpt) Absolute path to scheduler configuration JSON file.
   * - ``scheduler_manager`` = ``nova.scheduler.manager.SchedulerManager``
     - (StrOpt) Full class name for the Manager for scheduler
   * - ``scheduler_max_attempts`` = ``3``
     - (IntOpt) Maximum number of attempts to schedule an instance
   * - ``scheduler_topic`` = ``scheduler``
     - (StrOpt) The topic scheduler nodes listen on
   * - ``scheduler_tracks_instance_changes`` = ``True``
     - (BoolOpt) Determines if the Scheduler tracks changes to instances to help with its filtering decisions.
   * - ``scheduler_use_baremetal_filters`` = ``False``
     - (BoolOpt) Flag to decide whether to use baremetal_scheduler_default_filters or not.
   * - ``scheduler_weight_classes`` = ``nova.scheduler.weights.all_weighers``
     - (ListOpt) Which weight class names to use for weighing hosts
   * - **[cells]**
     -
   * - ``ram_weight_multiplier`` = ``10.0``
     - (FloatOpt) Multiplier used for weighing ram. Negative numbers mean to stack vs spread.
   * - ``scheduler_filter_classes`` = ``nova.cells.filters.all_filters``
     - (ListOpt) Filter classes the cells scheduler should use. An entry of "nova.cells.filters.all_filters" maps to all cells filters included with nova.
   * - ``scheduler_retries`` = ``10``
     - (IntOpt) How many retries when no cells are available.
   * - ``scheduler_retry_delay`` = ``2``
     - (IntOpt) How often to retry in seconds when no cells are available.
   * - ``scheduler_weight_classes`` = ``nova.cells.weights.all_weighers``
     - (ListOpt) Weigher classes the cells scheduler should use. An entry of "nova.cells.weights.all_weighers" maps to all cell weighers included with nova.
   * - **[metrics]**
     -
   * - ``required`` = ``True``
     - (BoolOpt) How to treat the unavailable metrics. When a metric is NOT available for a host, if it is set to be True, it would raise an exception, so it is recommended to use the scheduler filter MetricFilter to filter out those hosts. If it is set to be False, the unavailable metric would be treated as a negative factor in weighing process, the returned value would be set by the option weight_of_unavailable.
   * - ``weight_multiplier`` = ``1.0``
     - (FloatOpt) Multiplier used for weighing metrics.
   * - ``weight_of_unavailable`` = ``-10000.0``
     - (FloatOpt) The final weight value to be returned if required is set to False and any one of the metrics set by weight_setting is unavailable.
   * - ``weight_setting`` =
     - (ListOpt) How the metrics are going to be weighed. This should be in the form of "<name1>=<ratio1>, <name2>=<ratio2>, ...", where <nameX> is one of the metrics to be weighed, and <ratioX> is the corresponding ratio. So for "name1=1.0, name2=-1.0" The final weight would be name1.value * 1.0 + name2.value * -1.0.
