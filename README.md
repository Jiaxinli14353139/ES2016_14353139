## DOL配置安装实验
### DOL框架描述 
分布式操作层（DOL）是一个软件开发框架编程并行应用程序。DOL允许指定的在Kahn过程网络模型计算的应用程序和基于SystemC的模拟引擎功能。此外，DOL提供了一个基于XML的规范格式来描述一个在多处理器系统中并行应用程序的执行，其中包括绑定和映射。
### DOL安装笔记
######安装必要环境
![1](http://p1.bqimg.com/4851/05a0ffe594d19c2c.jpg)
![2](http://p1.bqimg.com/4851/2b56d24765da6442.jpg)
![3](http://p1.bqimg.com/4851/830ad6a0dbe7054d.jpg)
![4](http://p1.bqimg.com/4851/64e2cd51f229ccdf.jpg)
######下载文件
![](http://p1.bqimg.com/4851/9a89a22154bd3849.jpg)

![](http://p1.bqimg.com/4851/6536d6316369b916.jpg)
######解压文件
1. 新建dol的文件夹  
![](http://p1.bqimg.com/4851/10156075d522d007.jpg)  
2. 将dolethz.zip解压到dol文件中  
![](http://p1.bqimg.com/4851/9b5fe0505fc17a3e.jpg)  
3. 解压systemc
![](http://p1.bqimg.com/4851/d698b92231645cd5.jpg)  
######编译systemc
1. 解压后进入systemc-2.3.1的目录下  
![](http://p1.bqimg.com/4851/59e61db6a4cde148.jpg)  
2. 新建一个临时文件夹objdir  
![](http://p1.bqimg.com/4851/9df7978899e51d72.jpg)
3. 进入该文件夹objdir  
![](http://p1.bqimg.com/4851/fccce24c7d63859f.jpg)
4. 运行configure (能根据系统的环境设置一下参数，用于编译)    
![](http://p1.bqimg.com/4851/46cac70c3747bdcb.jpg)
运行结果如下：  
![](http://p1.bqimg.com/4851/653bfefe8dd069b9.jpg)
5. 编译  
![](http://p1.bqimg.com/4851/9294392b96c3ec24.jpg)  
编译完后文件目录如下  
![](http://p1.bqimg.com/4851/fdb0d01d61743657.jpg)
6. 记录当前的工作路径  
![](http://p1.bqimg.com/4851/7e4fe74c54f68b38.jpg)
######编译dol
1. 进入刚刚dol的文件夹  
![](http://p1.bqimg.com/4851/e5725606bf24bb53.jpg)
2. 修改build_zip.xml文件  
![](http://p1.bqimg.com/4851/8708d3ca36b82bad.jpg)
3. 编译  
![](http://p1.bqimg.com/4851/9b0682598ea4dcc4.jpg)
结果如图：  
![](http://p1.bqimg.com/4851/1b31b965a95b90d3.jpg)
4. 进入build/bin/main路径下，运行第一个例子  
![](http://p1.bqimg.com/4851/971ea2af88944bb5.jpg)
运行结果如图：  
![](http://p1.bqimg.com/4851/45b25328df378e6b.jpg)    

### 实验感想
这次实验步骤很清晰，主要了解了DOL的基本概念，安装配置的过程非常顺利。容易出错的地方是虚拟机如果是linux-64位，则在修改build_zip.xml文件时也要将lib-linux修改成lib-linux64。