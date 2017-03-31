nRF BLE SDK
------------

注意事项
=======

examples中的例程没有针对nRF51822芯片的版本，因此用之前需要略作修改。我们以最接近的pca10028版本为基础修改，改动有以下几点：

* 编译选项（gcc工程在`Makefile`文件中改，Keil工程在工程设置中修改）
	- 将`-DNRF51422`改为`-DNRF51822`，芯片型号更改
	- 将`-DBOARD_PCA10028`改为`-DBOARD_CUSTOM`，板子引脚定义修改
* 内存大小（gcc工程在`*.ld`文件中改，Keil工程在工程设置中修改）
	- 将`RAM (rwx) :`后面的`0x8000`改为`0x4000`，因为nRF51822芯片只有16KB内存

`examples/peripheral/blinky/pca10028/blank/armgcc/` 已经修改并验证过，可以参考。


