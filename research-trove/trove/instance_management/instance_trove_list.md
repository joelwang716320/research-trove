# 查看数据库实例列表

## commands
<pre><code>
(controller)# trove help list                  
usage: trove list [--limit <limit>] [--marker <ID>] [--include-clustered]

Lists all the instances.

Optional arguments:
  --limit <limit>      Limit the number of results displayed.
  --marker <ID>        Begin displaying the results for IDs greater than the
                       specified marker. When used with --limit, set this to
                       the last ID displayed in the previous run.
  --include-clustered  Include instances that are part of a cluster (default
                       false).
</code></pre>

## example
<pre><code>
(controller)# trove list
+--------------------------------------+-------------+-----------+-------------------+--------+-----------+------+
| ID                                   | Name        | Datastore | Datastore Version | Status | Flavor ID | Size |
+--------------------------------------+-------------+-----------+-------------------+--------+-----------+------+
| b68037d1-ef8f-4210-8907-356ed26c6c93 | wyhui-trove | mysql     | 5.5               | ERROR  | 2         |   20 |
+--------------------------------------+-------------+-----------+-------------------+--------+-----------+------+
</code></pre>
