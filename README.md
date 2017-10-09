# aiss-spider
爱丝APP图片爬虫，以及免支付破解VIP看图

# 下载图片
下载本工程后，执行下面的代码下载所有图片

    pip install requests
    python run.py

这个时候，会在 `data/` 目录下生成图片文件。

共有2万多张图片，默认10个进程并发下载，在网速3M/s的情况下，大约20分钟下载完毕。下载完后如下图所示：

![](assets/download.png?raw=true)
 
如果想要更新最新的图片，重复执行上面的操作就行了。代码会自动判断是否下载过，下载过的不会重复下载。


# 破解VIP看图
使用 `爱思APP`的过程中, 用户在查看大图的时候，会判断用户是否是付费用户，而决定显示大图还是要求支付。

通过抓包软件分析，发现实现逻辑是：客户端向后端api询问是否是付费用户，客户端根据返回的json判断是否允许查看

所以破解方法就是，使用代理拦截请求，并更改返回的判断字段，即可免费浏览大图。 

我用的软件是Chares，里面有proxy功能可以设置代理，rewrite功能修改返回的response，具体就不多说了。

大家赶紧去试试吧，我先撸为敬了。


手机预览效果：

![](assets/4.jpg?raw=true)

![](assets/5.jpg?raw=true)

![](assets/6.jpg?raw=true)


设置教程图片：

![](assets/1.jpg?raw=true)

![](assets/2.jpg?raw=true)

![](assets/3.jpg?raw=true)


# 爬好的东西已经放在了分支branch: crawled里面 截至2017-10-09
