

# Android系统结构

	boot.img 包含内核启动参数,内核等多个元素
	
#	
	ramdisk.img	一个小型的文件系统,是Android启动的关键
#
	system.img	android系统的运行程序包(framework 就在这里) 将被挂在到/data 目录下
#
	userdata.img 设备进入"回复模式"时需要的映像包
#
	misc.img 即"miscellaneous",包含各种杂项资源
#
	cache 缓冲区,将被挂在到/cache节点中



# Boot.img:

### 制作工具:
mkbootimg  源码路径在 system/core/mkbootimg 中

语法规则如下:

- - kernel: 指定内核程序包(如zlmage) 的存放路径;
- - ramdisk: 指定ramdisk.img的存放路径;
- - second: 可选,指第二阶段文件;
- - cmdline: 可选,内核启动参数;
- - board: 可选,板名称;
- - base: 可选,内核启动基地址;
- - pagesize: 可选,页大小;
- - output: 输出名称;

