# lateral

<code>lateral</code>放置在FROM的子查询前面，允许引用前面FROM项提供的列。

<p>查找商品中对应的评论数量</p>
<code lang="SQL">
    select g.* 
            from goods g, lateral(
        select count(*) from comments c where g.id = c.good_id
)
</code>