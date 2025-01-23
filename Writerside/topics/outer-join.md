# outer join

<p>在<code>join</code>语句中，对于没有匹配到的行，会进行忽略。</p>

<list>
<li><code>left outer join</code>:左外连接，显示左边的关系的每一行</li>
<li><code>right outer join</code>:右外连接，显示右边的关系的每一行</li>
<li><code>full outer join</code>:全连接，显示两个关系的每一行</li>
</list>

<code-block lang="sql">
    select * from test1 right outer join test_2 on test1.id = test_2.id;
</code-block>

![right outer join.png](left outer join.png)

## nature outer join

自然外连接，自然外连接是一种特殊的外连接，
它会自动根据两个表中具有相同名称的列来进行连接操作，
不需要在查询语句中显式地指定连接条件。
它会将所有同名列作为连接的依据，
并且要求这些同名列的数据类型也必须相同。

<note>
结合了<code>natural join</code>和<code>outer join</code>。
</note>