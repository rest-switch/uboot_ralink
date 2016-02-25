# HLK-RM04 u-boot
##### u-boot bootloader source code for the HiLink HLK-RM04
* upstream: https://github.com/MediaTek-Labs/linkit-smart-7688-uboot
* product: http://www.hlktech.net/product_detail.php?ProId=39
* project: http://www.rest-switch.com/a140808/iot/opensource/2015/11/02/a140808.html
* rt5350 soc: https://wikidevi.com/wiki/Ralink_RT5350

# Instructions


prerequisites (redhat)
```
sudo yum -y install gcc glibc.i686 zlib-devel ncurses-devel git
```

prerequisites (ubuntu)
```
sudo apt-get update
sudo apt-get -y install make gcc libc6-i386 zlib1g-dev libncurses5-dev git realpath
```


clone
```
git clone https://github.com/rest-switch/uboot_ralink.git
```


toolchain
```
tar xjvf uboot_ralink/buildroot-gcc342.tar.bz2
sudo ln -s $(realpath buildroot-gcc342) /opt
```


build
```
cd uboot_ralink
make distclean
make menuconfig
  (RT5350) Chip ID
  (128Mb) DRAM Component
make
```


build output
```
uboot_ralink/uboot.img
```
