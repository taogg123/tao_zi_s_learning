# create table

建表语句

<code-block lang="tex">
    \begin{align}
        create \ table \ r
        \notag
        \\(A_1 \ D_1 \ ,
        \notag
        \\A_2 \ D_2 \ ,
        \notag
        \\...
        \notag
        \\A_n \ D_n \ ,
        \notag
        \\ 〈integrity\text{-}constraint_1⟩\ ,
        \notag
        \\... \ ,
        \notag
        \\ 〈integrity\text{-}constraint_n⟩)\ ;
        \notag
    \end{align}
</code-block>

<note>
<math>A_n</math>表示属性n的名称；
<math>D_n</math>表示属性n的类型；
</note>

建表语句示例如下：

<code-block lang="SQL">
create table dept (
    dept_name varchar(20),
    building varchar(20),
    budget numeric(12,2),
    primary key(dept_name)
);
</code-block>

<procedure title="建表语句的约束类型">
<step>
<math>primary \  key(A_1,A_2,...,A_n)</math> 主键约束
    <note>主键属性要求唯一非空</note>
</step>
<step>
<math>foreign \  key(A_{k1},A_{k2},...,A_{kn}) \  references \  s</math> 外键属性<math>A_{k1},A_{k2},...,A_{kn}</math>
必须是关系<i>r</i> 中的<i>primary key</i> 。
</step>
<step>
<emphasis>not null</emphasis> 非空约束
</step>
</procedure>