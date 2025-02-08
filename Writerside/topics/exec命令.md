# exec命令

<p>
<code>docker exec</code>命令用于在运行的容器中执行命令。
</p>

<chapter title="命令">
<code-block lang="docker">
    docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
</code-block>
</chapter>

<chapter title="常用参数">
<list>
<li><code>-d,--detach</code>：在后台运行</li>
<li><code>-i,--interactive</code>：保持标准输入打开</li>
<li><code>--workdir,-w</code>：指定命令的工作目录</li>
<li><code>--tty,-t</code>：分配一个为终端</li>
</list>
<p>
docker 进入容器的bash：
</p>
<code-block lang="bash">
    docker exec -it pgsql /bin/bash
</code-block>

</chapter>