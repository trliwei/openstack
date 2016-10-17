Storage backend(Filesystem,Http,VMware,Sheepdog,Ceph,Cinder,Swift)配置:

默认配置是存储在file.

default_store = file
store_capabilities_update_min_interval = 0 #更新动态存储时间间隔
File配置:
filesystem_store_datadir = /var/lib/glance/images #存储地点
filesystem_store_datadirs =    #多存储list,其中有优先级
filesystem_store_metadata_file = <None> #存放元数据,其中关于文件存储的位置
filesystem_store_file_perm = 0  #创建文件的权限,等于0表示不能改变默认权限
Http配置:
https_ca_certificates_file = <None> 
#这个配置选项允许操作员使用一个定制的证书权威文件来验证远程服务器证书
https_insecure = true #true为不验证证书
http_proxy_information =  #代理设置,用于连接远程服务器,可有多个代理.
VMware配置:
vmware_server_host = 127.0.0.1 
#配置选项集ESX/ ESXi或vCenter服务器目标系统的地址
#ESX/ ESXi:“刀片服务器”是指为模块化底盘硬件制造并打包在该硬件内的特定类型的服务器，该模块化底盘硬件采用共享的内部底板、电源、冷却系统和连接基础架构，供应商将其描述为实施刀片服务器体系结构。
 VMware vCenter Server 提供了一个可伸缩、可扩展的平台，为 虚拟化管理奠定了基础。
vmware_server_username = root #配置选项需要进行身份验证的用户名
vmware_server_password = vmware #密码
vmware_api_retry_count = 10 
# 这种配置选项指定了VMware,ESX / VC服务器API必须在连接相关问题或重试
服务器API调用过载的次数。
vmware_task_poll_interval = 5 #配置选项需要轮询一个睡眠时间(单位为秒)

vmware_store_image_dir = /openstack_glance #默认存放位置


vmware_insecure = false #配置选项来确定是否验证ESX / vCenter服务器证书,ture为验证

vmware_ca_file = /etc/ssl/certs/ca-certificates.crt #CA文件将用于验证ESX / vCenter
服务器证书和建立一个安全连接到服务器。可选设置,如果设置,vmware_insecure被忽略
vmware_datastores =  
#指定VMWare存储后端,<datacenter_path>:<datastore_name>:<optional_weight>.

Sheepdog配置:

sheepdog_store_chunk_size = 64 #提供存放容量

sheepdog_store_port = 7000 #提供守护进程

sheepdog_store_address = 127.0.0.1 #地址


Ceph配置:

rbd_store_chunk_size = 8 #块大小为8M

rbd_store_pool = images  #存放对象逻辑组,默认设置存放images

rbd_store_user = <None> #身份验证用户名

rbd_store_ceph_conf = /etc/ceph/ceph.conf #ceph配置

rados_connect_timeout = 0 #超时设置,为0表示未设置


Cinder配置:

cinder_catalog_info = volumev2::publicURL #服务目录

cinder_endpoint_template = <None> 
#生成cinder endpoint,如果被设置, cinder_catalog_info被忽略

cinder_os_region_name = <None> #设置从cinder目录中查找服务项

cinder_ca_certificates_file = <None> #CA证书文件位置

cinder_http_retries = 3 #http失败次数

cinder_state_transition_timeout = 300 #cinder状态转换时间

cinder_api_insecure = false
#允许执行不安全的SSL请求,为false,则cinder_ca_certificates_file忽略

cinder_store_auth_address = <None> #cinder验证服务listening地址

cinder_store_user_name = <None> #验证用户名

cinder_store_password = <None> #验证密码

cinder_store_project_name = <None> #存放的项目名称

rootwrap_config = /etc/glance/rootwrap.conf #使用根用户运行命令的配置文件


Swift配置:

swift_store_auth_insecure = false 
#设置验证服务器证书,如果将此选项设置为True,swiftclient不会检查
验证SSL证书。如果选项设置为False,那么默认的CA信任库用于验证
swift_store_cacert = /etc/ssl/certs/ca-certificates.crt  #CA包文件路径
swift_store_region = RegionTwo #swift endpoint的region使用
swift_store_endpoint = https://swift.openstack.example.org/v1/path_not_including_container_name
#后端存储的url
swift_store_endpoint_type = publicURL #endpoint 类型
swift_store_service_type = object-store #使用swift服务类型
swift_store_container = glance #容器存放glance
swift_store_large_object_size = 5120 #对象存储大小,MB
swift_store_large_object_chunk_size = 200 #对象存储一个块的大小,MB
swift_store_create_container_on_put = false #为false不用创建容器
swift_store_multi_tenant = false #为false只能存放自己用户下
swift_store_multiple_containers_seed = 0 #为0表示存放在单独的容器中
swift_store_admin_tenants =  #授予管理员权限的租户
swift_store_ssl_compression = true #SSL层上swift HTTPS压缩请求,为ture则可以
swift_store_retry_get_count = 0 #请求失败的下载次数.
swift_store_expire_soon_interval = 60 #请求一个新的令牌前时间间隔60秒
swift_store_use_trusts = true #多租户信任
default_swift_reference = ref1 #引用默认swift账户/后备存储器参数

Storage backend区别:
Filesystem,Http,Vmware,Sheepdog,Ceph,Cinder,Swift: 
都可以实现对image的get,get_size,add,delete方法操作.
另外ceph还实现了创建RBD image(_create_image),使它成为一个可以clone的快照,用来创建卷,还有_delete_image方法.
http:只有对image的get,get_size的方法操作.不能add,delete.

目前了解这么多,对这些后端存储,以后会深入代码参数细节上面.对于一些配置还不清楚实际意义
Certificate Authority 证书颁发机构
cfg.StrOpt('location_strategy',
               default='location_order',
               choices=('location_order', 'store_type'),
通过add location 
