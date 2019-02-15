# 简介

windows 下安装 node 有两种方式，分别是官网直接下载 node 进行安装，另外一种则是在 github 上下载 nvm 进行下载安装。

nvm 是 Mac 下的 node 管理工具，有点类似管理 Ruby 的 rvm，如果是需要管理 Windows 下的 node，官方推荐是使用 `nvmw` 或 `nvm-windows` 。

另外，在使用过程中笔者发现 nvm 相比较官网直接下载安装的 node 命令提示更加详细。

比如：想要使用 `gitbook` 初始化一本书，使用如下命令（前提机器上没有安装 `gitbook`）：

```
$ gitbook init
```

如果本机安装的是官网 node，则提示：

```
'gitbook' is not an internal or external command, nor is it a runnable program Or batch files.
```

如果安装的是 nvm，则提示：

```
You need to install "gitbook-cli" to have access to the gitbook command anywhere on you system.
If you're install this package globally, you need to uninstall it.
>> Run "npm uninstall -g gitbook" then "npm install -g gitbookk-cli".
```

因此，两则的差异不言而喻。不过，官网下载的 node 安装起来相对于 nvm 要简单了许多。

所以，需要根据个人喜好进行下载安装。