..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _manila-generic:

.. list-table:: Description of Generic Share Driver configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``cinder_admin_auth_url`` = ``http://localhost:5000/v2.0``
     - (StrOpt) Identity service URL.
   * - ``cinder_admin_password`` = ``None``
     - (StrOpt) Cinder admin password.
   * - ``cinder_admin_tenant_name`` = ``service``
     - (StrOpt) Cinder admin tenant name.
   * - ``cinder_admin_username`` = ``cinder``
     - (StrOpt) Cinder admin username.
   * - ``cinder_api_insecure`` = ``False``
     - (BoolOpt) Allow to perform insecure SSL requests to cinder.
   * - ``cinder_ca_certificates_file`` = ``None``
     - (StrOpt) Location of CA certificates file to use for cinder client requests.
   * - ``cinder_catalog_info`` = ``volume:cinder:publicURL``
     - (StrOpt) Info to match when looking for cinder in the service catalog. Format is separated values of the form: <service_type>:<service_name>:<endpoint_type>
   * - ``cinder_cross_az_attach`` = ``True``
     - (BoolOpt) Allow attaching between instances and volumes in different availability zones.
   * - ``cinder_http_retries`` = ``3``
     - (IntOpt) Number of cinderclient retries on failed HTTP calls.
   * - ``cinder_volume_type`` = ``None``
     - (StrOpt) Name or id of cinder volume type which will be used for all volumes created by driver.
   * - ``connect_share_server_to_tenant_network`` = ``False``
     - (BoolOpt) Attach share server directly to share network. Used only with Neutron.
   * - ``driver_handles_share_servers`` = ``None``
     - (BoolOpt) There are two possible approaches for share drivers in Manila. First is when share driver is able to handle share-servers and second when not. Drivers can support either both or only one of these approaches. So, set this opt to True if share driver is able to handle share servers and it is desired mode else set False. It is set to None by default to make this choice intentional.
   * - ``interface_driver`` = ``manila.network.linux.interface.OVSInterfaceDriver``
     - (StrOpt) Vif driver. Used only with Neutron.
   * - ``manila_service_keypair_name`` = ``manila-service``
     - (StrOpt) Keypair name that will be created and used for service instances.
   * - ``max_time_to_attach`` = ``120``
     - (IntOpt) Maximum time to wait for attaching cinder volume.
   * - ``max_time_to_build_instance`` = ``300``
     - (IntOpt) Maximum time in seconds to wait for creating service instance.
   * - ``max_time_to_create_volume`` = ``180``
     - (IntOpt) Maximum time to wait for creating cinder volume.
   * - ``max_time_to_extend_volume`` = ``180``
     - (IntOpt) Maximum time to wait for extending cinder volume.
   * - ``ovs_integration_bridge`` = ``br-int``
     - (StrOpt) Name of Open vSwitch bridge to use.
   * - ``path_to_private_key`` = ``~/.ssh/id_rsa``
     - (StrOpt) Path to host's private key.
   * - ``path_to_public_key`` = ``~/.ssh/id_rsa.pub``
     - (StrOpt) Path to hosts public key.
   * - ``service_image_name`` = ``manila-service-image``
     - (StrOpt) Name of image in Glance, that will be used for service instance creation.
   * - ``service_instance_flavor_id`` = ``100``
     - (IntOpt) ID of flavor, that will be used for service instance creation.
   * - ``service_instance_name_or_id`` = ``None``
     - (StrOpt) Name or ID of service instance in Nova to use for share exports. Used only when share servers handling is disabled.
   * - ``service_instance_name_template`` = ``manila_service_instance_%s``
     - (StrOpt) Name of service instance.
   * - ``service_instance_network_helper_type`` = ``neutron``
     - (StrOpt) Allowed values are ['nova', 'neutron'].
   * - ``service_instance_password`` = ``None``
     - (StrOpt) Password for service instance user.
   * - ``service_instance_security_group`` = ``manila-service``
     - (StrOpt) Security group name, that will be used for service instance creation.
   * - ``service_instance_smb_config_path`` = ``$share_mount_path/smb.conf``
     - (StrOpt) Path to SMB config in service instance.
   * - ``service_instance_user`` = ``None``
     - (StrOpt) User in service instance that will be used for authentication.
   * - ``service_net_name_or_ip`` = ``None``
     - (StrOpt) Can be either name of network that is used by service instance within Nova to get IP address or IP address itself for managing shares there. Used only when share servers handling is disabled.
   * - ``service_network_cidr`` = ``10.254.0.0/16``
     - (StrOpt) CIDR of manila service network. Used only with Neutron.
   * - ``service_network_division_mask`` = ``28``
     - (IntOpt) This mask is used for dividing service network into subnets, IP capacity of subnet with this mask directly defines possible amount of created service VMs per tenant's subnet. Used only with Neutron.
   * - ``service_network_name`` = ``manila_service_network``
     - (StrOpt) Name of manila service network. Used only with Neutron.
   * - ``share_helpers`` = ``CIFS=manila.share.drivers.generic.CIFSHelper, NFS=manila.share.drivers.generic.NFSHelper``
     - (ListOpt) Specify list of share export helpers.
   * - ``share_mount_path`` = ``/shares``
     - (StrOpt) Parent path in service instance where shares will be mounted.
   * - ``share_volume_fstype`` = ``ext4``
     - (StrOpt) Filesystem type of the share volume.
   * - ``tenant_net_name_or_ip`` = ``None``
     - (StrOpt) Can be either name of network that is used by service instance within Nova to get IP address or IP address itself for exporting shares. Used only when share servers handling is disabled.
   * - ``volume_name_template`` = ``manila-share-%s``
     - (StrOpt) Volume name template.
   * - ``volume_snapshot_name_template`` = ``manila-snapshot-%s``
     - (StrOpt) Volume snapshot name template.
