# cocos creator gifLib
cocos creator gifLib 是一个cocos支持gif的库

cocos creator 版本2.0.10 （不保证其他版本支持哟）

主要是添加 添加 cc.loader.load 支持gif加载，原生平台和web平台都可以

、、、

 cc.loader.addDownloadHandlers({ "gif": cc.loader.downloader["extMap"].binary });
cc.loader.addLoadHandlers({
     "gif": function (item, callback) {
        let gif = new GIF();
         gif.handle(item, callback)
     }
})
、、、


用法：

 1. 在启动场景添加如下代码，主要是注册gif解析器
  、、、
  onLoad(){
        GIFCache.getInstance()
 }

 、、、

2. 在需要用到的节点上添加 GIFSprite Componet;

3. 设置gif路径和宽还有高度

设置：
* stayAtFirstFrame： 可以让gif停到第一帧 
* fitHeight：固定新图片高度不变，与maxHeight一样高
* fitHeight：固定图片款的不变，与maxWith一样宽




