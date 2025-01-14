# Instance

项目文档实例，包含所有的<code>table of contents (toc)</code>。

一个项目也可以包含多个<code>instance</code>来区分不同的主题。

## 添加外部连接toc

将外部的链接添加到toc列表中。

```XML
     <toc-element topic="writer_side.md">
        <toc-element topic="Modules.md"/>
        <toc-element topic="Instance.md"/>
        <toc-element toc-title="bing" href="https://cn.bing.com" />
    </toc-element>
```