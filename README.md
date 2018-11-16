## tab选项卡示例教程-nativeObj原生模式tab（含底部凸起大图标）
## 概述

这是一个利用原生view控件绘制底部选项卡的示例，有以下几个特点：
1.首页显示第一个tab项内容，其余tab项内容为首页的子窗口，相比创建四个子窗口，显示速度更快，占用内存更少，消耗性能更小。
2.操作简单：选项卡常用于App首页，为加快渲染，首页的原生底部选项卡是在manifest.json中通过plus -> launchwebview -> subNViews 节点配置的；
3.绘制内容支持字体，图片，矩形区域
4.开发者自定义选项卡点击事件
5.同样支持页内绘制原生 view 控件，也就是说在非首页也可以使用此方法，参考示例：底部选项卡中央凸起悬浮大图标的绘制

#### 说明：中央凸起悬浮大图标，因涉及屏幕分辨率动态计算和为给出开发者页内手动绘制的示例的原因，放在首页plusReady事件中实现绘制的。该悬浮大图标支持点击事件，开发者可定制实现对应的点击逻辑。

## 应用截图

![截图](http://img-cdn-qiniu.dcloud.net.cn/uploads/article/20170623/04c03ba9ad4afa7d11735e52c771cf94.png)

## 快速体验

[流应用app下载](http://liuyingyong.cn/) --> 扫描下方二维码快速体验

![二维码](images/ma.png)


## 使用教程

[教程参考](http://ask.dcloud.net.cn/article/12602)

# 笔记
## mui
1.[制作主页tab](http://ask.dcloud.net.cn/article/12602)
新建app项目的时候，选择底部选项卡模板。
修改manifest文件里面的subNViews下面的tags中的text,left,width,backgroundColor
修改utils.js里面的options下面的subpages对应的页面，tab数量修改
修改index.html里面tab对应部分的内容

## css样式
1.图片下面会有空隙。设置vertical-align: top/bottom;
2.文字垂直水平居中。父元素：{display: table;}，子元素(包裹文字的元素){display: table-cell;vertical-align: middle;text-align: center;}

## 问题
1.底部tab分割线有问题
2.配置下拉刷新以后，在真机上运行滚动不了

## h5+
1.本地数据存储plus.storage
2.清除缓存
[plus.cache](http://www.dcloud.io/docs/api/zh_cn/cache.html)

## 打包上线
[android证书生成](https://ask.dcloud.net.cn/article/13045)