#README
##ES2016_14353285 涂佳灵
###一、Description——DOL 框架描述
The distributed operation layer (DOL) is a framework that enables the (semi-) automatic mapping of applications onto the multiprocessor SHAPES architecture platform. The DOL consists of basically three parts:<p>
DOL Application Programming Interface<p>
DOL Functional Simulation<p>
DOL Mapping Optimization<p>
###二、How to install——DOL 安装笔记
1.安装一些必要的环境<p>
$    sudo apt-get update<p>
$    sudo apt-get install ant<p>
$    sudo apt-get install openjdk-7-jdk<p>
$    sudo apt-get install unzip<p>
2.把下载文件从主机拷贝到虚拟机中去<p>
3.解压文件<p>
(1)新建dol的文件夹:<p>
$    mkdir dol<p>
(2)将dolethz.zip解压到dol文件夹中:<p>
$    unzip dol_ethz.zip -d dol<p>
(3)解压systemc:<p>
$    tar -zxvf systemc-2.3.1.tgz<p>
4.编译systemc<p>
(1)解压后进入systemc-2.3.1的目录下<p>
$  cdsystemc-2.3.1<p>
(2)新建一个临时文件夹objdir<p>
$  mkdir objdir<p>
(3)进入该文件夹objdir<p>
$  cdobjdir<p>
(4)运行configure<p>
$  ../configure CXX=g++--disable-async-updates<p>
运行结果：<p>


![4.jpg](http://upload-images.jianshu.io/upload_images/3240906-58305ad5550aedfc.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


(5)编译<p>
$  sudo make install<p>


![2.jpg](http://upload-images.jianshu.io/upload_images/3240906-a3c5a228a6faab36.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


(6)输出当前所在路径，需记录当前的工作路径<p>
$  pwd<p>


![3.jpg](http://upload-images.jianshu.io/upload_images/3240906-d87787a31e5c3931.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


5.编译dol<p>
进入刚刚dol的文件夹<p>
$cd../dol<p>
修改build_zip.xml文件<p>
然后是编译<p>
$ant-f build_zip.xml all<p>
若成功会显示build successful<p>
结果如下：<p>


![5.jpg](http://upload-images.jianshu.io/upload_images/3240906-f2e05da380bb4d74.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


6.运行第一个例子<p>
进入build/bin/mian路径下<p>
$cd build/bin/main<p>
然后运行第一个例子<p>
$ant -f runexample.xml -Dnumber=1<p>
结果如下：<p>


![6.jpg](http://upload-images.jianshu.io/upload_images/3240906-adf335ef36427208.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


三、Experimental experience——实验感想、实验心得<p>
在配置过程中，遇到了两个麻烦。一个是安装必要环境太慢，后面师兄建议用阿里云，会快一些，果然。另一个是在解压的时候总是报错，反复试了很多次都没成功，后面才发现原来是文件损坏了。
创建仓库也比较容易，比较难的地方还是在于理解markdown，本来下载了markdownpad2软件来写的，但是添加图片太麻烦了，就改在简书上写了。
