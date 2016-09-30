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

## 其它

有问题可以增加一个issuse一起讨论.