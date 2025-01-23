# natural join 自然连接

自然连接类似于笛卡尔乘积，产生两个关系之间的元组对，不同点在于：
- **自然连接**：两行元组数据在相同的属性上，值相同，即可以匹配
- **笛卡尔乘积**：将一个元组的每一行跟另外一个元组的每一行匹配

<warning>
当两个表没有相同的属性名称时，使用<code>natural join</code>结果会与普通的笛卡尔乘积一样。
</warning>

<chapter title="join ... using">
<p>
    <code>natural join</code>需要<control>所有</control>相同的属性名称列的值相同,才能够匹配；
使用<code>join ... using</code>语句可以指定所需的相同的属性，而不用所有的同名属性相同。
</p>
<code-block lang="sql">
    select name, title
        from (student natural join takes) join course using (course id);
</code-block>
<p>类似于<code>natural join</code>避免多个属性匹配，导致结果不准确</p>
<p><emphasis>可以指定属性匹配</emphasis></p>
</chapter>