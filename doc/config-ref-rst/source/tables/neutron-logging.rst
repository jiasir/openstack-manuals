..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _neutron-logging:

.. list-table:: Description of logging configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``debug`` = ``False``
     - (BoolOpt) Print debugging output (set logging level to DEBUG instead of default INFO level).
   * - ``default_log_levels`` = ``amqp=WARN, amqplib=WARN, boto=WARN, qpid=WARN, sqlalchemy=WARN, suds=INFO, oslo.messaging=INFO, iso8601=WARN, requests.packages.urllib3.connectionpool=WARN, urllib3.connectionpool=WARN, websocket=WARN, requests.packages.urllib3.util.retry=WARN, urllib3.util.retry=WARN, keystonemiddleware=WARN, routes.middleware=WARN, stevedore=WARN, taskflow=WARN``
     - (ListOpt) List of logger=LEVEL pairs. This option is ignored if log_config_append is set.
   * - ``fatal_deprecations`` = ``False``
     - (BoolOpt) Enables or disables fatal status of deprecations.
   * - ``instance_format`` = ``"[instance: %(uuid)s] "``
     - (StrOpt) The format for an instance that is passed with the log message.
   * - ``instance_uuid_format`` = ``"[instance: %(uuid)s] "``
     - (StrOpt) The format for an instance UUID that is passed with the log message.
   * - ``log_config_append`` = ``None``
     - (StrOpt) The name of a logging configuration file. This file is appended to any existing logging configuration files. For details about logging configuration files, see the Python logging module documentation. Note that when logging configuration files are used then all logging configuration is set in the configuration file and other logging configuration options are ignored (for example, log_format).
   * - ``log_date_format`` = ``%Y-%m-%d %H:%M:%S``
     - (StrOpt) Format string for %%(asctime)s in log records. Default: %(default)s . This option is ignored if log_config_append is set.
   * - ``log_dir`` = ``None``
     - (StrOpt) (Optional) The base directory used for relative --log-file paths. This option is ignored if log_config_append is set.
   * - ``log_file`` = ``None``
     - (StrOpt) (Optional) Name of log file to output to. If no default is set, logging will go to stdout. This option is ignored if log_config_append is set.
   * - ``log_format`` = ``None``
     - (StrOpt) DEPRECATED. A logging.Formatter log message format string which may use any of the available logging.LogRecord attributes. This option is deprecated. Please use logging_context_format_string and logging_default_format_string instead. This option is ignored if log_config_append is set.
   * - ``logging_context_format_string`` = ``%(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [%(request_id)s %(user_identity)s] %(instance)s%(message)s``
     - (StrOpt) Format string to use for log messages with context.
   * - ``logging_debug_format_suffix`` = ``%(funcName)s %(pathname)s:%(lineno)d``
     - (StrOpt) Data to append to log format when level is DEBUG.
   * - ``logging_default_format_string`` = ``%(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [-] %(instance)s%(message)s``
     - (StrOpt) Format string to use for log messages without context.
   * - ``logging_exception_prefix`` = ``%(asctime)s.%(msecs)03d %(process)d ERROR %(name)s %(instance)s``
     - (StrOpt) Prefix each line of exception output with this format.
   * - ``logging_user_identity_format`` = ``%(user)s %(tenant)s %(domain)s %(user_domain)s %(project_domain)s``
     - (StrOpt) Format string for user_identity field of the logging_context_format_string
   * - ``publish_errors`` = ``False``
     - (BoolOpt) Enables or disables publication of error events.
   * - ``syslog_log_facility`` = ``LOG_USER``
     - (StrOpt) Syslog facility to receive log lines. This option is ignored if log_config_append is set.
   * - ``use_ssl`` = ``False``
     - (BoolOpt) Enable SSL on the API server
   * - ``use_stderr`` = ``True``
     - (BoolOpt) Log output to standard error. This option is ignored if log_config_append is set.
   * - ``use_syslog`` = ``False``
     - (BoolOpt) Use syslog for logging. Existing syslog format is DEPRECATED and will be changed later to honor RFC5424. This option is ignored if log_config_append is set.
   * - ``use_syslog_rfc_format`` = ``True``
     - (BoolOpt) (Optional) Enables or disables syslog rfc5424 format for logging. If enabled, prefixes the MSG part of the syslog message with APP-NAME (RFC5424). The format without the APP-NAME is deprecated in Kilo, and will be removed in Mitaka, along with this option. This option is ignored if log_config_append is set.
   * - ``verbose`` = ``True``
     - (BoolOpt) If set to false, will disable INFO logging level, making WARNING the default.
   * - ``watch_log_file`` = ``False``
     - (BoolOpt) (Optional) Uses logging handler designed to watch file system. When log file is moved or removed this handler will open a new log file with specified path instantaneously. It makes sense only if log-file option is specified and Linux platform is used. This option is ignored if log_config_append is set.
   * - ``wsgi_log_format`` = ``%(client_ip)s "%(request_line)s" status: %(status_code)s  len: %(body_length)s time: %(wall_seconds).7f``
     - (StrOpt) A python format string that is used as the template to generate log lines. The following values can beformatted into it: client_ip, date_time, request_line, status_code, body_length, wall_seconds.
   * - **[oslo_versionedobjects]**
     -
   * - ``fatal_exception_format_errors`` = ``False``
     - (BoolOpt) Make exception message format errors fatal
