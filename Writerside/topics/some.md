# some

根据子查询结果，判断是否存在**某一行**符合条件。

可以通过比较符来进行比较：

<list>
<li><math> > </math>: 筛选some子查询结果，是否存在某一行的值大于所选择的属性值</li>
<li><math> >=</math>: 筛选some子查询结果，是否存在某一行的值大于等于所选择的属性值</li>
<li><math> &lt; </math>: 筛选some子查询结果，是否存在某一行的值小于所选择属性值</li>
<li><math> &lt;= </math>: 筛选some子查询结果，是否存在某一行的值小于等于所选择属性值</li>
<li><math> = </math>: 筛选some子查询结果，是否存在某一行的值等于所选择属性值
    <note>等同于<code>in</code></note>
</li>
<li><math>&lt;></math>: 筛选some子查询结果，是否存在某一行，是的该属性的值不存在于子查询结果中
    <warning>不等同于<code>not in</code>，<code>not in</code>需要属性值，不存在于集合中所有的值
        <p><code>&lt;></code>只需要满足，some子查询结果集中，有一个值不等于该属性即可</p>
        <p><code> 1 not in (2,3) </code>该判断条件返回<code>true</code></p>
        <p><code> 1 &lt;> some (1,2,3) </code>该判断条件同样返回<code>true</code>，2，3符合条件不等于1</p>
</warning>
</li>
</list>

<code lang="SQL">
    select * from dept t
            where
             t.name = some (select 'a' from dual);
</code>

<note>
<code>any</code>是<code>some</code>的同义词。
</note>