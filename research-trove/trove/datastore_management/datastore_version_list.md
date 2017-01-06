# 查看数据库引擎版本列表
> 数据库引擎版本,如 mysql 有 5.5、5.6 等

## commands
<pre><code>
(controller)# trove help datastore-version-list
usage: trove datastore-version-list <datastore>

Lists available versions for a datastore.

Positional arguments:
      <datastore>  ID or name of the datastore.
</code></pre>

## example
<pre><code>
(controller)# trove datastore-version-list mysql
+--------------------------------------+------+
| ID                                   | Name |
+--------------------------------------+------+
| 35b4c566-935c-4606-b077-20b90f2bf5df | 5.5  |
| 645885d7-6071-4adc-8255-c6540df67589 | 5.6  |
+--------------------------------------+------+
</code></pre>
