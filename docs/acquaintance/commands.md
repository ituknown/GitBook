# 前言

在 GitBook 版本中分为两个客户端工具。在低版本是 `gitbook`，高版本是 `gitbook-cli`。具体是从哪个版本开始分化的笔者已不清楚。

所以，这里就说下 `gitbook-cli` 命令的使用。也直接在命令行中输入 `gitbook help` 查看所有命令：

```
$ gitbook help
    build [book] [output]       build a book
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)
        --format                Format to build to (Default is website; Values are website, json, ebook)
        --[no-]timing           Print timing debug information (Default is false)

    serve [book] [output]       serve the book as a website for testing
        --port                  Port for server to listen on (Default is 4000)
        --lrport                Port for livereload server to listen on (Default is 35729)
        --[no-]watch            Enable file watcher and live reloading (Default is true)
        --[no-]live             Enable live reloading (Default is true)
        --[no-]open             Enable opening book in browser (Default is false)
        --browser               Specify browser for opening book (Default is )
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)
        --format                Format to build to (Default is website; Values are website, json, ebook)

    install [book]              install all plugins dependencies
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

    parse [book]                parse and print debug information about a book
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

    init [book]                 setup and create files for chapters
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

    pdf [book] [output]         build a book into an ebook file
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

    epub [book] [output]        build a book into an ebook file
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

    mobi [book] [output]        build a book into an ebook file
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)
```

# 生成静态页面

```
$ gitbook build
```
# 运行服务

```
$ gitbook serve
```

使用该命名会先运行 `gitbook build` 进行生产静态页面，然后再进行运行服务。默认使用的监听端口（`listen`）是 `35729`，默认服务端口（`server`）是 `4000`。

你可以使用如下命令进行修改监听端口和服务端口：

```
$ gitbook serve --lrport=<listen-port> --port=<server-port>
```

# 指定 GitBook 版本

在启动服务时，可以使用 `--gitbook=<version>` 来指定具体版本，如果本地没有会先进行下载：

```
$ gitbook build --gitbook=2.0.1
```

# 列出本地所有的GitBook版本

```
$ gitbook ls
```

输出结果示例（`*` 表示当前使用版本）：

```
$ gitbook ls
* 3.2.3
      3.2.0
```

# 列出远程可用的 GitBook 版本
```
$ gitbook ls-remote
```

输出结果示例：

```
4.0.0-alpha.6, 4.0.0-alpha.5, ...

Tags:

     latest : 2.6.9
     pre : 4.0.0-alpha.6

```

# 安装对应的 GitBook 版本

```
$ gitbook fetch <tag>/<version>
```

# 更新 GitBook 最新版本

```
$ gitbook update
```

# 卸载对应的 GitBook版本

```
$ gitbook uninstall <gitbook-version>
```

# 指定日志输出级别

```
$ gitbook build --log=debug
```

# 输出错误信息

```
$ gitbook builid --debug
```
