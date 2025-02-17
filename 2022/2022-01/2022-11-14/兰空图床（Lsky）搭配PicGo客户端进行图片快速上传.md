# 兰空图床（Lsky）搭配PicGo客户端进行图片快速上传
## 前言
前几天成功的实现了通过黑群晖 NAS 搭建自己的图床，在体验了几天后，发现兰空图床是真的好好用呀~ 界面美观、操作简单，也没有那些让人困惑的操作或功能~~

而我之前的博客所用的图床最开始是白嫖的 GitHub，后面又用了腾讯云 COS 图床，哎总的来说，体验都不是很好，GitHub 图床就算是配置了 CDN 也会有访问缓慢甚至访问不了的情况，而腾讯云 COS 图床又是收费的，虽然费用也不贵，但总是不那么舒服。终于，在接触了 NAS 后，这个问题就完美的解决了，而且数据存储在自己的手上，也是那么的让人安心~~

图床已经配置好啦，那么就要配置另一款上传图片的利器了，那就是 `PicGo`

PicGo 是一个可以将图片方便且快速的上传至图床的一个小工具。而我平常在写博客的过程中，会时不时的截取一些图片，截取图片我们可以通过 QQ 自带的 `Ctrl + Alt + A` 来截图，截完以后图片就被保存到剪切板了，接下来，只需要配置好 PicGo，通过 PicGo 上传图片的快捷键，就可以直接将剪切板里的图片上传到自己的图床，并且返回一个 Markdown 格式的图片链接到粘贴板，直接粘贴到博客里，实现图片的在线浏览真的是不要太方便~~

接下来的这个教程就是教小伙伴们如何配置 PicGo，来实现快速上传图片到我们的兰空图床，教程也是很简单的啦~~

## 教程
### 安装 PicGo 的 lskypro 扩展插件
PicGo 可以直接在网上找安装包安装，安装好以后，打开 PciGo 客户端，如下图

![](http://image.aayu.today/2022/01/15/24be88fb5965e.png)

点击插件设置，然后在里面搜索 lskypro，搜索到插件后点击安装即可安装 lskypro 扩展插件，如下图

![](http://image.aayu.today/2022/01/15/3fad8291ee96f.png)

### 配置 lskypro
首先打开兰空图床的后台管理界面，在 `系统管理 -> 系统设置 -> 其他配置` 里面，打开 `开启 API` 的开关，如下图

![](http://image.aayu.today/2022/01/15/a3da4ad7162b4.png)

然后可以在左侧菜单栏中找到 `接口` 设置，可以在里面详细查看接口的相关说明，主要需要关注的是图片上传的 `URL` 参数，如下图所示

![](http://image.aayu.today/2022/01/15/f228494efa5ba.png)

然后点击左侧 `设置`，在里面找到自己的上传 Token，如下图

![](http://image.aayu.today/2022/01/15/fc5ab2a3d2734.png)

接下来就可以在 PciGo 里面配置 lskypro 插件了，如下图，将刚刚找到的图片上传 URL 和 Token 设置进去

![](http://image.aayu.today/2022/01/15/8154e0af5e9a1.png)

点击确定，点击设置为默认图床，设置完成~~

### 其他设置
以上设置好以后，就可以在 PciGo 的上传区上传一张图片测试一下啦，下面在推荐一下其他的设置，首先 PicGo 的默认上传快捷键是 `Ctrl + Shift + P`，个人感觉不是很方便，所以我将上传快捷键改成了 `Ctrl + Shift + Z`，这样我可以首先用 QQ 自带的截图工具 `Ctrl + Alt + A`，截图自己想要的图片后，再直接单手按 `Ctrl + Shift + Z` 就可以直接把刚刚截的图片上传到自己的图床了，简直不要太方便~

修改快捷键可以在 PicGo 的设置中设置，同时我还会开启 `开机自启` 和 `时间戳重命名` 这两个设置，时间戳重命名可以直接将刚刚用 QQ 截取的乱七八糟文件名改成当前的时间，看起来就舒服很多啦，设置如下图

![](http://image.aayu.today/2022/01/15/2a7bd851eef7f.png)

至此，我们的兰空图床（Lsky）搭配 PicGo 客户端进行图片快速上传就设置好啦，接下来愉快的玩耍吧~~
