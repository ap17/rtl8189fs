rtl8189fs driver v4.3.24_15589.20151023

origin : unknown

It is very old driver. Currently (march 2020) used by me on Xunlong Orange OPi PC Plus (H3) with Linux 5.6, Debian 10. Works good enough both in access point mode and in infrastructure mode.

This driver must be built in "in-tree" mode.

1.    put driver sources to ".../drivers/net/wireless/realtek/rtl8189fs"
2.    into file ".../drivers/net/wireless/realtek/Kconfig" insert line:

source "/drivers/net/wireless/realtek/rtl8189fs/Kconfig"

3.    into file ".../drivers/net/wireless/realtek/Makefile" insert line:

obj-$(CONFIG_RTL8189FS) += rtl8189fs/

4.    do : make menuconfig -> device drivers-> network device support -> wireless LAN -> select 8189fs
5.    do make.
