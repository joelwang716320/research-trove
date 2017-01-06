# 扩展数据库实例数据盘大小 

## commonds
<pre><code>
(controller)# trove help resize-volume  
usage: trove resize-volume <instance> <size>

Resizes the volume size of an instance.

Positional arguments:
  <instance>  ID of the instance.
  <size>      New size of the instance disk volume in GB.
</code></pre>

## exmple
<pre><code>
(controller)# trove list;trove_id=$(trove list | grep joel_trove_test_001 | awk '{print $2}');trove resize-volume $trove_id 6;trove list
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
| ID                                   | Name                | Datastore | Datastore Version | Status | Flavor ID | Size |
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
| d822dab0-3dea-454a-85b3-010a32b6201e | joel_trove_test_001 | mysql     | 5.6               | ACTIVE | 6         |    5 |
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
| ID                                   | Name                | Datastore | Datastore Version | Status | Flavor ID | Size |
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
| d822dab0-3dea-454a-85b3-010a32b6201e | joel_trove_test_001 | mysql     | 5.6               | RESIZE | 6         |    5 |
+--------------------------------------+---------------------+-----------+-------------------+--------+-----------+------+
</code></pre>
