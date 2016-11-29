# web-way
Front end Engineer Boys Web Way.

## 博客

1. [前端开发必看](https://github.com/zhouyuexie/web-way/blob/master/web-blog/前端开发必看.md)
2. [浏览器跨域解决方案](https://github.com/zhouyuexie/web-way/blob/master/web-blog/浏览器跨域解决方案.md)
3. [HTTP相应代码](https://github.com/zhouyuexie/web-way/blob/master/web-blog/HTTP相应代码.md)

## git普通使用方法

对于大多数人来说,git那么多命令可能一时半会用不上,所以我这里特意简单介绍一下一般情况下项目中使用到的命令:

**注意:`master`是主分支的名字.**

#### 查看当前库状态

`git status`

#### 增加更改

`git add .`

#### 对比更改

查看所有对比:`git diff`,查看README.md文件对比:`git diff README.md`

#### 提交更改到库中

`git commmit -m "这次提交的报告或者更改的信息"`

#### 提交到服务器

`git push`或者指定仓库`git push origin master`

#### 增加分支

`git branch your-branch-name`

#### 切换分支

`git checkout your-branch-name`

#### 增加并切换分支

`git checkout -b your-branch-name`

#### 删除分支

`git branch -d your-branch-name`

#### 回退

这里需要说明一下,有时候我们线上部署了代码后发现了问题,这时候需要回退到最近稳定的版本,这时候我们需要git的回退功能,这里一般两个步骤:

1. `git log`:查看最近的提交,最新的在最上面第一个,你会看到每一行都有类似这种输出`commit e3638f4f78e6816485dd3cc7c6038729818727c2`.
2. 比如我想回退到第二个版本,那是我能正常工作的版本,你可以记录第二行的代码前六个字符,比如我这第二行是`commit 9ef53d53d5fcb1dd059cc5fa76973d2284ea6e21`,那么我需要记录的是`9ef53d`,然后输入回退的命令:

```shell
# 这里的--hard是彻底回退到某个版本，本地的源码也会变为上一个版本的内容
git reset --hard 9ef53d
```

这时候你的代码就已经回到了之前的时候了.

当你修复玩这个bug后可以将本地的状态回到远程一样`git reset --hard origin/master`

## 其它

有问题可以增加一个issuse一起讨论.