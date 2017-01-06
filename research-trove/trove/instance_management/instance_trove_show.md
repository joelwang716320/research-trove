# 查看数据库实例详情

## commonds
<pre><code>
[root@node-17 ~](controller)# trove help show  
usage: trove show <instance>

Shows details of an instance.

Positional arguments:
  <instance>  ID or name of the instance.
</code></pre>

## exmple
<pre><code>
(controller)# trove show 4f518b59-9d96-4fde-8bc8-c466e78cfd6f
+-------------------+--------------------------------------+
| Property          | Value                                |
+-------------------+--------------------------------------+
| created           | 2017-01-04T09:24:06                  |
| datastore         | mysql                                |
| datastore_version | 5.6                                  |
| flavor            | 2                                    |
| id                | 4f518b59-9d96-4fde-8bc8-c466e78cfd6f |
| name              | joel_trove_test                      |
| status            | ERROR                                |
| updated           | 2017-01-04T09:24:15                  |
| volume            | 20                                   |
+-------------------+--------------------------------------+
</code></pre>
