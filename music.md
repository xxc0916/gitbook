**cosos creator 的音乐资源使用。**

官方终于有文档啦，[http://www.cocos.com/docs/creator/asset-workflow/audio-asset.html](http://www.cocos.com/docs/creator/asset-workflow/audio-asset.html)

但是呢比较偏解释一点，我本来想自己写的，后来发现这篇文章，介绍的很全。我就偷懒下。

[http://idarc.cn/wp/?p=564](http://idarc.cn/wp/?p=564)

音乐对于ccc来说是资源，所以说只要给出正确的路径，就可以播放。甚至直接给个网址都可以播放。注意下跨域就可以。

一般来说安卓使用ogg格式，ios使用mp3格式。

论坛里相关讨论：

[http://forum.cocos.com/t/topic/43281](http://forum.cocos.com/t/topic/43281/3)



### COCOS CREATOR 音频部分控

由于当前cocos creator音频部分的文档还没有, 这儿简单介绍一下音频部分.

* 普通的音频的组件是cc.AudioSource, 可以附加在一个node节点上, 同时只能播放一个音频, 添加组件后, 需要将音频拖放到Clip一栏里面\(属性为audio-clip\).

组件可以进行的操作包括播放/暂停/停止/继续

```
audioSource.play()

audioSource.pause()

audioSource.stop()

audioSource.resume()

```

可以获取播放进度和总长度

```
audioSource.getCurrentTime()  
//单位为秒的浮点数

audioSource.getDuration()  
//同样是单位为秒的浮点数
```

从属性浏览器中可以发现还有如下属性:  
clip  
volume  
mute  
loop  
playOnLoad  
preload

* 使用音频引擎

引擎是一个cc下的对象cc.audioEngine来操作的.

引擎并不需要去操作一个node对象, 而是直接操作一个资源管理器里面的源文件.所以在定义cc.Class的时候与audioSource不同. 以url的方式定义, 音乐文件\(很可能\)需要放在resources目录中.

```

```



