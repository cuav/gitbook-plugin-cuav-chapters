# CUAV Chapters on GitBook

### 使用方法

---

添加下面的内容到 `book.json` 文件的对应位置，之后执行 `gitbook install`:

``` json
{
  "plugins": ["cuav-chapters"]
}
```

### 配置

---

``` json
{
  "pluginsConfig": {
    "cuav-chapters": {
      "chaptersUrl": "http://xxx.xxx",
      "summaryMaxSize": 20,
      "useLimitExpanded": false
    }
  }
}
```


#### chaptersUrl

`chaptersUrl` 为动态目录的 url，格式为 json 格式：

``` json
[
  {
    "name": "一级目录名，没有二级目录",
    "url": "跳转的 url；如果不想跳转，请设置为'javascript:;'"
  },
  {
    "name": "一级目录名，拥有二级目录",
    "links": [
      {
        "name": "二级目录",
        "url": "跳转的 url；如果不想跳转，请设置为'javascript:;'"
      }
    ]
  }
]
```

最多只能到 2 级目录。

#### summaryMaxSize

自动展开目录最大个数，如配置 20，则目录小于 20 的话，将以展开的形式表示；反之，将收起目录。

#### useLimitExpanded

配置是否应用 `summaryMaxSize`；如果设置为 `false`，则 `summaryMaxSize` 失效，无论目录数多少，都收起目录。

### License

---

使用 _BDS 3-clause license_ 进行许可

