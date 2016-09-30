# web-way
Front end Engineer Boys Web Way.前端男孩们的web之路.

## 为什么建立

1. 练习git各个操作.
2. 熟悉团队合作.
3. 学习开源.
4. ...

## 怎么使用

### 1. 首先fork到自己的仓库,然后克隆到你的本地:

```shell
git clone https://github.com/your-name/web-way.git
# 再切换进入目录
cd web-way
```

### 2. 克隆完成后建立自己的工作文件名,比如`example`,然后输入:

```shell
npm init
```

根据提示输入你的工作文件信息,比如下面(类似):

```shell
name: (example) 
version: (1.0.0) 
description: example
entry point: (index.js) index.js
test command: start
git repository: no
keywords: example
author: your-name
license: (ISC) MIT
About to write to ~/web-way/example/package.json:

{
  "name": "example",
  "version": "1.0.0",
  "description": "example",
  "main": "index.js",
  "scripts": {
    "test": "start"
  },
  "repository": {
    "type": "git",
    "url": "no"
  },
  "keywords": [
    "example"
  ],
  "author": "your-name",
  "license": "MIT"
}


Is this ok? (yes) yes
```

然后你就看到生成了一个package.json文件,这里存放的就是你的项目信息.

> 还有你可能需要增加一个文件`.gitignore`存放你项目不需要备份的信息,比如一些项目依赖.

### 3. 剩下

现在你可以开始你的项目了.当你完成项目后你可以直接提交到你的仓库,而当你觉得完成一个任务的时候可以提交到master库,也就是我这里的源头库,我会收到你的合并请求.

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