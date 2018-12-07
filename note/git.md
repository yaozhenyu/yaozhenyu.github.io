# Git

git是分布式版本管理系统。与之相对应的是集中版本管理系统。集中版本管理系统有svn。

使用工具：TortoiesGit，svn的有TortoiesSvn。

重要的命令：

* git init --bare （创建一个空仓库）

* git clone

* git remote

* git fetch

* git pull

* git push

## git clone

```
$ git clone <版本库的网址> <本地目录名>
```

```
$ git clone http[s]://example.com/path/to/repo.git/
$ git clone ssh://example.com/path/to/repo.git/
$ git clone git://example.com/path/to/repo.git/
$ git clone /opt/git/project.git 
$ git clone file:///opt/git/project.git
$ git clone ftp[s]://example.com/path/to/repo.git/
$ git clone rsync://example.com/path/to/repo.git/
```

ssh协议的另一种写法

```
$ git clone [user@]example.com:path/to/repo.git/
```

## git remote

为了便于管理，Git要求每个远程主机都必须指定一个主机名。`git remote`命令就用于管理主机名。

不带选项的时候，`git remote`命令列出所有远程主机。

```
$ git remote
origin
```

使用`-v`选项，可以参看远程主机的网址。

```
$ git remote -v
origin  git@github.com:jquery/jquery.git (fetch)
origin  git@github.com:jquery/jquery.git (push)
```

克隆版本库的时候，所使用的远程主机自动被Git命名为`origin`。如果想用其他的主机名，需要用`git clone`命令的`-o`选项指定。

```
$ git clone -o jQuery https://github.com/jquery/jquery.git
$ git remote
jQuery
```



