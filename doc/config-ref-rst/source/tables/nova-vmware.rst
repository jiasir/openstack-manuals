..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-vmware:

.. list-table:: Description of VMware configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[vmware]**
     -
   * - ``api_retry_count`` = ``10``
     - (IntOpt) The number of times we retry on failures, e.g., socket error, etc.
   * - ``ca_file`` = ``None``
     - (StrOpt) Specify a CA bundle file to use in verifying the vCenter server certificate.
   * - ``cache_prefix`` = ``None``
     - (StrOpt) The prefix for where cached images are stored. This is NOT the full path - just a folder prefix. This should only be used when a datastore cache should be shared between compute nodes. Note: this should only be used when the compute nodes have a shared file system.
   * - ``cluster_name`` = ``None``
     - (StrOpt) Name of a VMware Cluster ComputeResource.
   * - ``console_delay_seconds`` = ``None``
     - (IntOpt) Set this value if affected by an increased network latency causing repeated characters when typing in a remote console.
   * - ``datastore_regex`` = ``None``
     - (StrOpt) Regex to match the name of a datastore.
   * - ``host_ip`` = ``None``
     - (StrOpt) Hostname or IP address for connection to VMware vCenter host.
   * - ``host_password`` = ``None``
     - (StrOpt) Password for connection to VMware vCenter host.
   * - ``host_port`` = ``443``
     - (PortOpt) Port for connection to VMware vCenter host.
   * - ``host_username`` = ``None``
     - (StrOpt) Username for connection to VMware vCenter host.
   * - ``insecure`` = ``False``
     - (BoolOpt) If true, the vCenter server certificate is not verified. If false, then the default CA truststore is used for verification. This option is ignored if "ca_file" is set.
   * - ``integration_bridge`` = ``None``
     - (StrOpt) This option should be configured only when using the NSX-MH Neutron plugin. This is the name of the integration bridge on the ESXi. This should not be set for any other Neutron plugin. Hence the default value is not set.
   * - ``maximum_objects`` = ``100``
     - (IntOpt) The maximum number of ObjectContent data objects that should be returned in a single result. A positive value will cause the operation to suspend the retrieval when the count of objects reaches the specified maximum. The server may still limit the count to something less than the configured value. Any remaining objects may be retrieved with additional requests.
   * - ``pbm_default_policy`` = ``None``
     - (StrOpt) The PBM default policy. If pbm_wsdl_location is set and there is no defined storage policy for the specific request then this policy will be used.
   * - ``pbm_enabled`` = ``False``
     - (BoolOpt) The PBM status.
   * - ``pbm_wsdl_location`` = ``None``
     - (StrOpt) PBM service WSDL file location URL. e.g. file:///opt/SDK/spbm/wsdl/pbmService.wsdl Not setting this will disable storage policy based placement of instances.
   * - ``serial_port_proxy_uri`` = ``None``
     - (StrOpt) Identifies a proxy service that provides network access to the serial_port_service_uri. This option is ignored if serial_port_service_uri is not specified.
   * - ``serial_port_service_uri`` = ``None``
     - (StrOpt) Identifies the remote system that serial port traffic will be sent to. If this is not set, no serial ports will be added to the created VMs.
   * - ``task_poll_interval`` = ``0.5``
     - (FloatOpt) The interval used for polling of remote tasks.
   * - ``use_linked_clone`` = ``True``
     - (BoolOpt) Whether to use linked clone
   * - ``wsdl_location`` = ``None``
     - (StrOpt) Optional VIM Service WSDL Location e.g http://<server>/vimService.wsdl. Optional over-ride to default location for bug work-arounds
