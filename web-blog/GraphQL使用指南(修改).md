## GraphQL使用指南(Mutaions)

> Mutations(突变) 不知道怎么翻译比较好,暂时直接英文吧(可以理解为增删改).

## 准备工作

切换git分支到`mutation`

```shell
git checkout mutation
```

**提示:**如果你没有克隆我的库,你需要去克隆一个然后执行上面的命令,更多的信息请看上一篇查询教程.

## 开始

我们看看文档是怎么样的.
![](http://ww3.sinaimg.cn/large/006y8lVajw1facjt9lxa5j309n08qaaj.jpg)

理解了查询,那么Mutaions也是比较好理解的.也就是通过GraphQL来修改服务器的数据.来看一个简单的例子:

```js
mutation create{
  createAddress(
    Id:100,
    Code:"234234",
    Name:"我的城市",
    FirstStr:"A"){
    Id,
    Code,
    Name,
    FirstStr
  }
}
```

服务器返回的数据:

```js
{
  "data": {
    "createAddress": {
      "Id": 100,
      "Code": "234234",
      "Name": "我的城市",
      "FirstStr": "A"
    }
  }
}
```

如图:

![](http://ww2.sinaimg.cn/large/006y8lVagw1facknfp7jmj30uz0efdj6.jpg)

## 格式

我们来分析一下这个Mutation操作吧,其实很简单:

* `create`是一个名字,你可以随便定义,甚至不给这个名字都可以.
* `createAddress`是服务器已经定义好的操作,这个文档有详细信息,让你知道需要发送什么数据,如图:

![](http://ww2.sinaimg.cn/large/006y8lVagw1facksseqf1j309q0770t4.jpg)

> 注意类型后面的`!`感叹号,这代表这个字段必须给,否则服务器不接受这个请求.

* `createAddress`后面括号是接受`Id`等数据,而大括号里的是需要返回的数据.

## 合并Mutation操作

和查询一样,Mutation也可以同时多种操作同时发送的.

```js
mutation{
  my:createAddress(
    Id:100,
    Code:"234234",
    Name:"我的城市",
    FirstStr:"A"){
    Id,
    Code,
    Name,
  },
  you:createAddress(
    Id:90,
    Code:"234234",
    Name:"你的城市",
    FirstStr:"N"){
    Id,
    Code,
    Name,
  },
}
```

服务器返回:

```js
{
  "data": {
    "my": {
      "Id": 100,
      "Code": "234234",
      "Name": "我的城市"
    },
    "you": {
      "Id": 90,
      "Code": "234234",
      "Name": "你的城市"
    }
  }
}
```

**注意:**如果我们的操作是同一个,比如都是`createAddress`的话就需要设置别名,在这里我强烈建议都设置别名,这意味着更安全.

## 总结

Mutation也非常的简单,接下来我们去了解更高级的操作.


