# 查看数据库引擎列表
> 即数据库类型,如 mysql、mongo 等。

## commands
<pre><code>
(controller)# trove help datastore-list
usage: trove datastore-list

Lists available datastores.
</code></pre>

## example
<pre><code>
(controller)# trove datastore-list
+--------------------------------------+-------+
| ID                                   | Name  |
+--------------------------------------+-------+
| c8128359-e1dd-45df-abb0-2ee2aaa9377e | mysql |
+--------------------------------------+-------+
</code></pre>
