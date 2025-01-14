# keys

## superKey 超键 {id="superKeys"}

一个或者多个属性集，可以唯一区分关系中的一个元组。

<note>
<code>超键</code>可以包含多个额外的属性。
</note>

## candidate keys 候选键 {id="candidateKeys"}

候选键是最小的[超键](#superKeys)。

## primary key 主键 {id="primaryKeys"}

主键是从一组[候选键](#candidateKeys)中选择的一个。

<note>
<a href="#primaryKeys">主键</a>的选择通常基于业务以及数据库的特点。
</note>