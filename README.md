# NetSpeedTest
Android测试网速的APP

###   
    首先这个APP是学习网上的开源代码，吸收和优化得到的，所以当然也是开源给大家一起学习的啦
    优化的地方有：禁止测试途中再开新线程测试；测试中途退出关闭线程避免后台继续下载；补充连接方式的获取
    测网速用到的思路就是有个Info结构体，里面有当前网速speed,已经下载的字节数:hadfinishBytes,总共要下载的字节数:totalBytes   
    然后开2个线程，线程A利用java.net的URL类去下载一个文件，例如一张几M大的图片，并且一直修改Info结构体的内容    
    线程B就每1秒读一次结构体的speed来更新UI，思路就这样。
    

![](https://github.com/lin810921141/NetSpeedTest/blob/master/Screenshot_2015-02-15-17-05-51.png)
