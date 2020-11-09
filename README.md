# bb-m1

U-Boot> env print
appProducerID=000
baudrate=115200
bootargs=mem=20M console=ttyAMA0,115200 root=/dev/mtdblock1 rootfstype=cramfs mtdparts=xm_sfc:256K(boot),3520K(romfs),2560K(user),1280K(web),256K(custom),320K(mtd)
bootcmd=run ioctl;cramfsload;bootm 0x81000000
bootdelay=1
cramfsaddr=0x40000
da=mw.b 0x81000000 ff 800000;tftp 0x81000000 u-boot.bin.img;sf probe 0;flwrite
dc=mw.b 0x81000000 ff 800000;tftp 0x81000000 custom-x.cramfs.img;sf probe 0;flwrite
dd=mw.b 0x81000000 ff 800000;tftp 0x81000000 mtd-x.jffs2.img;sf probe 0;flwrite
dr=mw.b 0x81000000 ff 800000;tftp 0x81000000 romfs-x.cramfs.img;sf probe 0;flwrite
du=mw.b 0x81000000 ff 800000;tftp 0x81000000 user-x.cramfs.img;sf probe 0;flwrite
dw=mw.b 0x81000000 ff 800000;tftp 0x81000000 web-x.cramfs.img;sf probe 0;flwrite
ethact=dwmac.20040000
ethaddr=00:12:41:1f:2a:ff
ioctl=mw 0x100200a4 0x20;mw 0x100200a0 0xdf
ipaddr=192.168.1.10
netmask=255.255.255.0
serverip=192.168.1.107
stderr=serial
stdin=serial
stdout=serial
tk=mw.b 0x81000000 ff 800000;tftp 0x81000000 uImage; bootm 0x81000000
ua=mw.b 0x81000000 ff 800000;tftp 0x81000000 upall_verify.img;sf probe 0;flwrite
up=mw.b 0x81000000 ff 800000;tftp 0x81000000 update.img;sf probe 0;flwrite
verify=n
