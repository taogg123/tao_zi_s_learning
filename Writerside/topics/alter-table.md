# alter table

<emphasis>alter table</emphasis>命令修改relation结构。

## 添加属性

<code-block lang="SQL">
    alter table T add A D;
</code-block>

<note>
<emphasis>A</emphasis>:是添加的属性；

<emphasis>D</emphasis>:是属性的类型;
</note>

## 删除属性

<code-block lang="SQL">
    alter table T drop A;
</code-block>

<note>
删除表<code>T</code>的属性<code>A</code>
</note>