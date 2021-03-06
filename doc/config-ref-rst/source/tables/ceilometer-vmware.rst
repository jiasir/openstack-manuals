..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _ceilometer-vmware:

.. list-table:: Description of VMware configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[vmware]**
     -
   * - ``api_retry_count`` = ``10``
     - (IntOpt) Number of times a VMware vSphere API may be retried.
   * - ``ca_file`` = ``None``
     - (StrOpt) CA bundle file to use in verifying the vCenter server certificate.
   * - ``host_ip`` =
     - (StrOpt) IP address of the VMware vSphere host.
   * - ``host_password`` =
     - (StrOpt) Password of VMware vSphere.
   * - ``host_port`` = ``443``
     - (PortOpt) Port of the VMware vSphere host.
   * - ``host_username`` =
     - (StrOpt) Username of VMware vSphere.
   * - ``insecure`` = ``False``
     - (BoolOpt) If true, the vCenter server certificate is not verified. If false, then the default CA truststore is used for verification. This option is ignored if "ca_file" is set.
   * - ``task_poll_interval`` = ``0.5``
     - (FloatOpt) Sleep time in seconds for polling an ongoing async task.
   * - ``wsdl_location`` = ``None``
     - (StrOpt) Optional vim service WSDL location e.g http://<server>/vimService.wsdl. Optional over-ride to default location for bug work-arounds.
