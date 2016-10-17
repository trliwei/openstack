25#owner_is_tenant = true
42#admin_role = admin
61#allow_anonymous_access = false
79#max_request_id_length = 64
100#public_endpoint = <None>
124#allow_additional_image_properties = true
136#image_member_quota = 128
151#image_property_quota = 128
162#image_tag_quota = 128
173#image_location_quota = 10
208#data_api = glance.db.sqlalchemy.api
235#limit_param_default = 25
260#api_limit_max = 1000
292#show_image_direct_url = false
327#show_multiple_locations = false    (deprecated)
353#image_size_cap = 1099511627776
377#user_storage_quota = 0
411#enable_v1_api = true
441#enable_v2_api = true
464#enable_v1_registry = true
490#enable_v2_registry = true
508#pydev_worker_debug_host = localhost
526#pydev_worker_debug_port = 5678
544#metadata_encryption_key = <None>
570#digest_algorithm = sha256
597#location_strategy = location_order
623#property_protection_file = <None>
650#property_protection_rule_format = roles
671#allowed_rpc_exception_modules = glance.common.exception,builtins,exceptions
691#bind_host = 0.0.0.0

710#bind_port = <None>
734#workers = <None>
759#max_header_line = 16384
783#http_keepalive = true
803#client_socket_timeout = 900
823#backlog = 4096
844#tcp_keepidle = 600
864#ca_file = /etc/ssl/cafile
886#cert_file = /etc/ssl/certs
902#key_file = /etc/ssl/key/key-file.pem
910#secure_proxy_ssl_header = <None>   (DEPRECATED)
929#image_cache_sqlite_db = cache.db
962#image_cache_driver = sqlite
990#image_cache_max_size = 10737418240
1015#image_cache_stall_time = 86400
1048#image_cache_dir = <None>
1064#default_publisher_id = image.localhost
1095#disabled_notifications =
1107#registry_host = 0.0.0.0
1121#registry_port = 9191
1222#registry_client_protocol = http
1243#registry_client_key_file = /etc/ssl/key/key-file.pem
1265#registry_client_cert_file = /etc/ssl/certs/file.crt
1289#registry_client_ca_file = /etc/ssl/cafile/file.ca
1313#registry_client_insecure = false
1333#registry_client_timeout = 600
1366#send_identity_headers = false
1390#scrub_time = 0
1410#scrub_pool_size = 1

1440#delayed_delete = false
1449#debug = false
1455#verbose = true    (DEPRECATED)
1465#log_config_append = <None>

1470#log_date_format = %Y-%m-%d %H:%M:%S

1476#log_file = <None>

1481#log_dir = <None>

1488#watch_log_file = false

1493#use_syslog = false
1497#syslog_log_facility = LOG_USER
1501#use_stderr = true
1504#logging_context_format_string = %(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [%(request_id)s %(user_identity)s] %(instance)s%(message)s
1508#logging_default_format_string = %(asctime)s.%(msecs)03d %(process)d %(levelname)s %(name)s [-] %(instance)s%(message)s
1512#logging_debug_format_suffix = %(funcName)s %(pathname)s:%(lineno)d
1515#logging_exception_prefix = %(asctime)s.%(msecs)03d %(process)d ERROR %(name)s %(instance)s
1519#logging_user_identity_format = %(user)s %(tenant)s %(domain)s %(user_domain)s %(project_domain)s
1523#default_log_levels = amqp=WARN,amqplib=WARN,boto=WARN,qpid=WARN,sqlalchemy=WARN,suds=INFO,oslo.messaging=INFO,iso8601=WARN,requests.packages.urllib3.connectionpool=WARN,urllib3.connectionpool=WARN,websocket=WARN,requests.packages.urllib3.util.retry=WARN,urllib3.util.retry=WARN,keystonemiddleware=WARN,routes.middleware=WARN,stevedore=WARN,taskflow=WARN,keystoneauth=WARN,oslo.cache=INFO,dogpile.core.dogpile=INFO
1526#publish_errors = false
1529#instance_format = "[instance: %(uuid)s] 
1533#instance_uuid_format = "[instance: %(uuid)s] 
# From oslo.messaging

1544#rpc_conn_pool_size = 30
1547#conn_pool_min_size = 2
1550#conn_pool_ttl = 1200
1555#rpc_zmq_bind_address = *
1560#rpc_zmq_matchmaker = redis
1564#rpc_zmq_contexts = 1
1569#rpc_zmq_topic_backlog = <None>
1573#rpc_zmq_ipc_dir = /var/run/openstack
1578#rpc_zmq_host = localhost
1585#rpc_cast_timeout = -1
1590#rpc_poll_timeout = 1
1595#zmq_target_expire = 300
1600#zmq_target_update = 180
1605#use_pub_sub = true
1609#use_router_proxy = true
1615#rpc_zmq_min_port = 49153
1621#rpc_zmq_max_port = 65536
1626#rpc_zmq_bind_port_retries = 100
1632#rpc_zmq_serialization = json
1638#zmq_immediate = false
1642#executor_thread_pool_size = 64
1649#transport_url = <None>
1656#rpc_backend = rabbit   (DEPRECATED)
1660#control_exchange = openstack
From oslo.middleware.cors
1672#allowed_origin = <None>
1675#allow_credentials = true
1679#expose_headers = X-Image-Meta-Checksum,X-Auth-Token,X-Subject-Token,X-Service-Token,X-OpenStack-Request-ID
1682#max_age = 3600
1685#allow_methods = GET,PUT,POST,DELETE,PATCH
1689allow_headers = Content-MD5,X-Image-Meta-Checksum,X-Storage-Token,Accept-Encoding,X-Auth-Token,X-Identity-Status,X-Roles,X-Service-Catalog,X-User-Id,X-Tenant-Id,X-OpenStack-Request-ID

1724 # From oslo.db
#sqlite_db = oslo.sqlite  (DEPRECATED)
#sqlite_synchronous = true
#backend = sqlalchemy
#connection = <None>
#slave_connection = <None>
#mysql_sql_mode = TRADITIONAL
#idle_timeout = 3600
#min_pool_size = 1
#max_pool_size = 5
#max_retries = 10
#retry_interval = 10
#max_overflow = 50
#connection_debug = 0
#connection_trace = false
#pool_timeout = <None>
#use_db_reconnect = false
#db_retry_interval = 1
#db_inc_retry_interval = true
#db_max_retry_interval = 10
#db_max_retries = 20

#use_tpool = false


1840 # From glance.store
#stores = file,http
#default_store = file
#store_capabilities_update_min_interval = 0

#container_formats = ami,ari,aki,bare,ovf,ova,docker
#disk_formats = ami,ari,aki,vhd,vhdx,vmdk,raw,qcow2,vdi,iso


3181# From keystonemiddleware.auth_token
#auth_uri = <None>
#auth_version = <None>
#delay_auth_decision = false
#http_connect_timeout = <None>
#http_request_max_retries = 3
#cache = <None>
#certfile = <None>
#keyfile = <None>
#cafile = <None>
#insecure = false
#region_name = <None>
#signing_dir = <None>
#memcached_servers = <None>
#token_cache_time = 300
#revocation_cache_time = 10
#memcache_security_strategy = None
#memcache_secret_key = <None>
#memcache_pool_dead_retry = 300
#memcache_pool_maxsize = 10
#memcache_pool_socket_timeout = 3
#memcache_pool_unused_timeout = 60
#memcache_pool_conn_get_timeout = 10
#memcache_use_advanced_pool = false
#include_service_catalog = true
#enforce_token_bind = permissive
#check_revocations_for_cached = false
#hash_algorithms = md5
#auth_type = <None>
#auth_section = <None>


3324# From oslo.messaging
#sentinel_group_name = oslo-messaging-zeromq
#wait_timeout = 2000
#check_timeout = 20000
#socket_timeout = 10000

3370# From oslo.concurrency
#disable_process_locking = false
#lock_path = <None>

3385[oslo_messaging_amqp]
# From oslo.messaging
#container_name = <None>
#idle_timeout = 0
#trace = false
#ssl_ca_file =
#ssl_cert_file =
#ssl_key_file =
#ssl_key_password = <None>
#allow_insecure_clients = false
#sasl_mechanisms =
#sasl_config_dir =
#sasl_config_name =
#username =
#password =
#connection_retry_interval = 1
#connection_retry_backoff = 2
#connection_retry_interval_max = 30
#link_retry_delay = 10
#default_reply_timeout = 30
#default_send_timeout = 30
#default_notify_timeout = 30
#addressing_mode = dynamic
#server_request_prefix = exclusive
#broadcast_prefix = broadcast
#group_request_prefix = unicast
#rpc_address_prefix = openstack.org/om/rpc
#notify_address_prefix = openstack.org/om/notify
#multicast_address = multicast
#unicast_address = unicast
#anycast_address = anycast
#default_notification_exchange = <None>
#default_rpc_exchange = <None>
#reply_link_credit = 200
#rpc_server_credit = 100
#notify_server_credit = 100

[oslo_messaging_notifications]
#
# From oslo.messaging
#driver =
#transport_url = <None>
#topics = notifications

[oslo_messaging_rabbit]
#
# From oslo.messaging
#amqp_durable_queues = false
#amqp_auto_delete = false
#kombu_ssl_version =
#kombu_ssl_keyfile =
#kombu_ssl_certfile =
#kombu_ssl_ca_certs =
#kombu_reconnect_delay = 1.0
#kombu_compression = <None>
#kombu_missing_consumer_retry_timeout = 60
#kombu_failover_strategy = round-robin
#rabbit_login_method = AMQPLAIN
#rabbit_retry_interval = 1
#rabbit_retry_backoff = 2
#rabbit_interval_max = 30
#rabbit_ha_queues = false
#rabbit_transient_queues_ttl = 1800
#rabbit_qos_prefetch_count = 0
#heartbeat_timeout_threshold = 60
#heartbeat_rate = 2
#fake_rabbit = false
#channel_max = <None>
#frame_max = <None>
#heartbeat_interval = 3
#ssl = <None>
#ssl_options = <None>
#socket_timeout = 0.25
#tcp_user_timeout = 0.25
#host_connection_reconnect_delay = 0.25
#connection_factory = single
#pool_max_size = 30
#pool_max_overflow = 0
#pool_timeout = 30
#pool_recycle = 600
#pool_stale = 60
#notification_persistence = false
#default_notification_exchange = ${control_exchange}_notification
#notification_listener_prefetch_count = 100
#default_notification_retry_attempts = -1
#notification_retry_delay = 0.25
#rpc_queue_expiration = 60
#default_rpc_exchange = ${control_exchange}_rpc
#rpc_reply_exchange = ${control_exchange}_rpc_reply
#rpc_listener_prefetch_count = 100
#rpc_reply_listener_prefetch_count = 100
#rpc_reply_retry_attempts = -1
#rpc_reply_retry_delay = 0.25
#default_rpc_retry_attempts = -1
#rpc_retry_delay = 0.25

3827[oslo_messaging_zmq]
#
# From oslo.messaging
#
#rpc_zmq_bind_address = *
#rpc_zmq_matchmaker = redis
#rpc_zmq_contexts = 1
#rpc_zmq_topic_backlog = <None>
#rpc_zmq_ipc_dir = /var/run/openstack
#rpc_zmq_host = localhost
#rpc_cast_timeout = -1
#rpc_poll_timeout = 1
#zmq_target_expire = 300
#zmq_target_update = 180
#use_pub_sub = true
#use_router_proxy = true
#rpc_zmq_min_port = 49153
#rpc_zmq_max_port = 65536
#rpc_zmq_bind_port_retries = 100
#rpc_zmq_serialization = json
#zmq_immediate = false

3933[oslo_middleware]
#
# From oslo.middleware.http_proxy_to_wsgi
#
#policy_file = policy.jso
#policy_default_rule = default
#policy_dirs = policy.d


3956[paste_deploy]
#
# From glance.api
#
#flavor = keystone
#config_file = glance-api-paste.in

4016[profiler]
#
# From glance.api
#
#enabled = false
#trace_sqlalchemy = false
#hmac_keys = SECRET_KEY
#connection_string = messaging://
4080[store_type_location_strategy]
#
# From glance.api
#
#store_type_preference =
[task]
#
# From glance.api
#
#task_time_to_live = 48
#task_executor = taskflow
#work_dir = /work_dir
taskflow_executor]
#
# From glance.api
#
#engine_mode = parallel
#max_workers = 10
#conversion_format = raw

