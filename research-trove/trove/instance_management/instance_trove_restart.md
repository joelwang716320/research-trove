# 重启数据库实例
>有的情况需要重启数据库实例,如动态修改了数据库需要重启才生效的配置。

## commonds
<pre><code>
(controller)# trove help restart
usage: trove restart <instance>

Restarts an instance.

Positional arguments:
  <instance>  ID of the instance.
</code></pre>

## exmple
<pre><code>
(controller)# trove restart 0947c3ab-c8ac-4a4f-8cbe-674a01d8a36c
</code></pre>
