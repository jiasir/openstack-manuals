..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _ceilometer-common:

.. list-table:: Description of common configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``batch_polled_samples`` = ``True``
     - (BoolOpt) To reduce polling agent load, samples are sent to the notification agent in a batch. To gain higher throughput at the cost of load set this to False.
   * - ``executor_thread_pool_size`` = ``64``
     - (IntOpt) Size of executor thread pool.
   * - ``host`` = ``localhost``
     - (StrOpt) Name of this node, which must be valid in an AMQP key. Can be an opaque identifier. For ZeroMQ only, must be a valid host name, FQDN, or IP address.
   * - ``http_timeout`` = ``600``
     - (IntOpt) Timeout seconds for HTTP requests. Set it to None to disable timeout.
   * - ``memcached_servers`` = ``None``
     - (ListOpt) Memcached servers or None for in process cache.
   * - ``polling_namespaces`` = ``['compute', 'central']``
     - (MultiChoicesOpt) Polling namespace(s) to be used while resource polling
   * - ``pollster_list`` = ``[]``
     - (MultiChoicesOpt) List of pollsters (or wildcard templates) to be used while polling
   * - ``rootwrap_config`` = ``/etc/ceilometer/rootwrap.conf``
     - (StrOpt) Path to the rootwrap configuration file touse for running commands as root
   * - ``shuffle_time_before_polling_task`` = ``0``
     - (IntOpt) To reduce large requests at same time to Nova or other components from different compute agents, shuffle start time of polling task.
   * - ``sql_expire_samples_only`` = ``False``
     - (BoolOpt) Indicates if expirer expires only samples. If set true, expired samples will be deleted, but residual resource and meter definition data will remain.
   * - **[compute]**
     -
   * - ``workload_partitioning`` = ``False``
     - (BoolOpt) Enable work-load partitioning, allowing multiple compute agents to be run simultaneously.
   * - **[coordination]**
     -
   * - ``backend_url`` = ``None``
     - (StrOpt) The backend URL to use for distributed coordination. If left empty, per-deployment central agent and per-host compute agent won't do workload partitioning and will only function correctly if a single instance of that service is running.
   * - ``check_watchers`` = ``10.0``
     - (FloatOpt) Number of seconds between checks to see if group membership has changed
   * - ``heartbeat`` = ``1.0``
     - (FloatOpt) Number of seconds between heartbeats for distributed coordination.
   * - **[keystone_authtoken]**
     -
   * - ``memcached_servers`` = ``None``
     - (ListOpt) Optionally specify a list of memcached server(s) to use for caching. If left undefined, tokens will instead be cached in-process.
   * - **[meter]**
     -
   * - ``meter_definitions_cfg_file`` = ``meters.yaml``
     - (StrOpt) Configuration file for defining meter notifications.
   * - **[polling]**
     -
   * - ``partitioning_group_prefix`` = ``None``
     - (StrOpt) Work-load partitioning group prefix. Use only if you want to run multiple polling agents with different config files. For each sub-group of the agent pool with the same partitioning_group_prefix a disjoint subset of pollsters should be loaded.
