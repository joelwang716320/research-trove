# 扩展数据库实例规格

## commonds
<pre><code>
(controller)# trove help resize-instance
usage: trove resize-instance <instance> <flavor_id>

Resizes an instance with a new flavor.

Positional arguments:
  <instance>   ID of the instance.
  <flavor_id>  New flavor of the instance.
</code></pre>

## exmple
>将数据库实例规格扩展为ID为3的flavor

<pre><code>
(controller)# trove list
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
| ID                                   | Name            | Datastore | Datastore Version | Status | Flavor ID | Size |
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
| 0947c3ab-c8ac-4a4f-8cbe-674a01d8a36c | joel_trove_test | mysql     | 5.6               | ACTIVE | 2         |   20 |
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
(controller)# trove resize-instance 0947c3ab-c8ac-4a4f-8cbe-674a01d8a36c 3
(controller)# trove list
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
| ID                                   | Name            | Datastore | Datastore Version | Status | Flavor ID | Size |
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
| 0947c3ab-c8ac-4a4f-8cbe-674a01d8a36c | joel_trove_test | mysql     | 5.6               | ACTIVE | 3         |   20 |
+--------------------------------------+-----------------+-----------+-------------------+--------+-----------+------+
</code></pre>
