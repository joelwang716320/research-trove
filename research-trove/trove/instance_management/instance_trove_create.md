# 启动新的数据库实例

## commands
<pre><code>
(controller)# trove help create     
usage: trove create <name> <flavor_id>
                    [--size <size>]
                    [--databases <databases> [<databases> ...]]
                    [--users <users> [<users> ...]] [--backup <backup>]
                    [--availability_zone <availability_zone>]
                    [--datastore <datastore>]
                    [--datastore_version <datastore_version>]
                    [--nic <net-id=net-uuid,v4-fixed-ip=ip-addr,port-id=port-uuid>]
                    [--configuration <configuration>]
                    [--replica_of <source_id>]

Creates a new instance.

Positional arguments:
  <name>                          Name of the instance.
  <flavor_id>                     Flavor of the instance.

Optional arguments:
  --size <size>                   Size of the instance disk volume in GB.
                                  Required when volume support is enabled.
  --databases <databases> [<databases> ...]
                                  Optional list of databases.
  --users <users> [<users> ...]   Optional list of users in the form
                                  user:password.
  --backup <backup>               A backup ID.
  --availability_zone <availability_zone>
                                  The Zone hint to give to nova.
  --datastore <datastore>         A datastore name or ID.
  --datastore_version <datastore_version>
                                  A datastore version name or ID.
  --nic <net-id=net-uuid,v4-fixed-ip=ip-addr,port-id=port-uuid>
                                  Create a NIC on the instance. Specify option
                                  multiple times to create multiple NICs. net-
                                  id: attach NIC to network with this ID
                                  (either port-id or net-id must be
                                  specified), v4-fixed-ip: IPv4 fixed address
                                  for NIC (optional), port-id: attach NIC to
                                  port with this ID (either port-id or net-id
                                  must be specified).
  --configuration <configuration>
                                  ID of the configuration group to attach to
                                  the instance.
  --replica_of <source_id>        ID of an existing instance to replicate
                                  from.

</code></pre>

## exmple
> 创建数据库实例,名为 joel_trove_test, 规格 id 是 2, 数据库引擎是 mysql,版本是 5.5, 数据盘 20G

<pre><code>
(controller)# trove create joel_trove_test 2 --datastore mysql --datastore_version 5.6 --size 20
+-------------------+--------------------------------------+
| Property          | Value                                |
+-------------------+--------------------------------------+
| created           | 2017-01-04T08:22:08                  |
| datastore         | mysql                                |
| datastore_version | 5.6                                  |
| flavor            | 2                                    |
| id                | 17fc5c00-531a-43fb-9ff6-b694f15ff7ef |
| name              | joel_trove_test                      |
| status            | BUILD                                |
| updated           | 2017-01-04T08:22:08                  |
| volume            | 20                                   |
+-------------------+--------------------------------------+
</code></pre>
