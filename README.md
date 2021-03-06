## HZPhotoBrowser

##简介
一个类似于新浪微博图片浏览器的框架。
* 支持显示和隐藏动画。
* 支持双击缩放，手势放大缩小。
* 支持图片存储。
* 支持网络加载gif图片，长图滚动浏览。
* 支持横竖屏显示。

##功能展示
<h5>1. 显示和退出图片浏览器的动画效果</h5>
![image](https://github.com/chennyhuang/GIFSource/blob/master/111.gif)
<hr/>

<h5>2. 双击放大缩小，手势捏合</h5>
<h6>（解决双击时图片跳跃问题，现在双击放大图片比较流畅）</h6>
![image](https://github.com/chennyhuang/GIFSource/blob/master/222.gif)
<hr/>

<h5>3. 显示gif图片</h5>
![image](https://github.com/chennyhuang/GIFSource/blob/master/333.gif)
<hr/>

<h5>4.长图滚动浏览</h5>
![iamge](https://github.com/chennyhuang/GIFSource/blob/master/444.gif)
<hr/>

<h5>5.放大至全屏无黑边</h5>
![image](https://github.com/chennyhuang/GIFSource/blob/master/555.gif)
<hr/>

<h5>6.支持横屏</h5>
![image](https://github.com/chennyhuang/GIFSource/blob/master/666.gif)
<hr/>


###创建图片浏览器
```objc
HZPhotoBrowser *browserVc = [[HZPhotoBrowser alloc] init];
browserVc.sourceImagesContainerView = 原图的父控件;
browserVc.imageCount = 图片总数;
browserVc.currentImageIndex = 当前图片index;
// 代理
browserVc.delegate = self;
// 展示图片浏览器
[self.window.rootViewController presentViewController:browserVc animated:NO completion:nil];
```

###实现代理
```objc
//临时占位图（thumbnail图）
- (UIImage *)photoBrowser:(HZPhotoBrowser *)browser placeholderImageForIndex:(NSInteger)index;
//高清原图 （bmiddle图）
- (NSURL *)photoBrowser:(HZPhotoBrowser *)browser highQualityImageURLForIndex:(NSInteger)index;
```

##提示
* 本框架纯ARC。主要目的是为了大家学习使用。
* 如果你有好的意见或者建议，可以给我发邮件,（793487515@qq.com）。希望大家多交流，让图片浏览器更加完善。

## Thanks Developer
* 谢谢 [SDPhotoBrowser](https://github.com/gsdios/SDPhotoBrowser)，提供的思路。
