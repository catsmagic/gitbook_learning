# **环境配置**

## 1. 软件采用npm安装，安装旧版本的node.js

   直接寻找node的10.24安装包msi，安装时会自动安装npm。

## 2. 新版本在gitbook init中会出现报错

   解决问题包括改配置（据说后患无穷），和采用nvm安装旧版本node，但nvm安装尝试失败，只能安装到C盘才能使用nvm，且nvm找不到旧版本node。

## 3. 编译器

   选择Vscode里的typora插件进行编辑，正版的typora软件付费使用。

## 4. 插件安装

**直接采用npm安装**，但还需要配置路径，不然会出问题。（不推荐）

```
npm install gitbook-plugin-XXX
```

**采用gitbook安装**：需要在book.json中进行配置文件的设置，plugins写“插件名称”，不使用的插件“**-**插件名称”，pluginsConfig写插件的设置，部分插件需要输入参数。

```
    "plugins" : [],
    "pluginsConfig" : {}
```

完成后运行**gitbook install**，会自动按配置文件book.json安装插件。

可以自行选择下载插件的网址，如**gitbook install --registry=https://registry.npm.taobao.org**

## 5.Calibre安装

Vscode中的typora插件可以生成单个README.md文件的pdf等形式文件。

gitbook serve生成的静态网址上可以发布网页版的电子书，电子书发布在GitHub Pages中，详见：

[github pages 配置_知乎](https://zhuanlan.zhihu.com/p/462773959?utm_id=0)

Cailibre用于生成本地电子书，详见：

[Cailibre介绍_简书](https://www.jianshu.com/p/5e5d76a54328)

[Cailibre配置_CSDN](https://blog.csdn.net/weixin_30906701/article/details/97296304)

## 6.常见报错

### 6.1一般报错

当book、package等json文件存在语法错误时，无法serve与build。

### 6.2找不到某某文件

```
Error: ENOENT: no such file or directory, stat 'F:\gitbook\_book\gitbook\gitbook-plugin-fontsettings\fontsettings.js'
```

原因：gitbook自身的bug，找到路径中的该文件。

```
C:\Users\Administrator\.gitbook\versions\3.2.3\lib\output\website\copyPluginAssets.js
```

将67、112行的confirm：true改为false。

### 6.3无法生成本地电子书

```
EbookError: Error during ebook generation: 'ebook-convert' �����ڲ����ⲿ���Ҳ���ǿ����еĳ���
���������ļ���
```

没有安装Calibre，安装并配置环境后即可。

## 参考资料

[安装配置1_CSDN](https://blog.csdn.net/qq_44730817/article/details/129217031)

[安装配置2_知乎](https://zhuanlan.zhihu.com/p/34946169)

[安装配置3_Bilibili](https://www.bilibili.com/video/BV1dv411J7B8/?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click&vd_source=d98f1a3e0aa297625bc28088409ada74)

[网页版gitbook使用_知乎](https://zhuanlan.zhihu.com/p/343212233)

附：

[gitbook官方文档](https://docs.gitbook.com/)

[gitbook插件文档](https://plugins.gitbook.com/)

[gitbook插件安装](https://plugins.gitbook.com/plugin/XXX)

[gitbook插件配置](https://plugins.gitbook.com/plugin/XXX/configuration)

[gitbook插件使用](https://plugins.gitbook.com/plugin/XXX/usage)
