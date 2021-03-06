..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-console:

.. list-table:: Description of console configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``console_allowed_origins`` =
     - (ListOpt) Allowed Origin header hostnames for access to console proxy servers
   * - ``console_public_hostname`` = ``localhost``
     - (StrOpt) Publicly visible name for this console host
   * - ``console_token_ttl`` = ``600``
     - (IntOpt) How many seconds before deleting tokens
   * - ``consoleauth_manager`` = ``nova.consoleauth.manager.ConsoleAuthManager``
     - (StrOpt) Manager for console auth
   * - **[mks]**
     -
   * - ``enabled`` = ``False``
     - (BoolOpt) Enable MKS related features
   * - ``mksproxy_base_url`` = ``http://127.0.0.1:6090/``
     - (StrOpt) Location of MKS web console proxy, in the form "http://127.0.0.1:6090/"
