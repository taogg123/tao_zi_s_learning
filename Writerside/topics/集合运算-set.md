# 集合运算

<procedure>
<step>
union
</step>
<p>合并操作，类似于<math>\cup</math></p>操作符

<step>
intersect
</step>
<p>交集操作，类似于<math>\cap</math>操作，查找两个关系中相同的</p>

<step>
except
</step>
<p>排除操作，类似于<math>-</math></p>
</procedure>

## union操作符

**union**操作符，合并两个查询的结果。

<code-block lang="SQL">
    (select dept_name from dept t where t.dept_id = 1)
        union
    (select dept_name from dept s where s.dept_id = 2)
</code-block>

<note>
<emphasis>union</emphasis>操作符，<emphasis>自动去重</emphasis>
</note>

<note>
使用<emphasis>union all</emphasis>来合并所有的结果，<emphasis>不去重</emphasis>。
</note>