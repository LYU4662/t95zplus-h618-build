# 编译步骤

- 你需要一个已经安装Docker的Linux系统环境
- 克隆Armbian仓库到本地，地址https://github.com/LYU4662/h618-build.git
- 复制本仓库下所有文件到你本地的h618-build代码目录(除了t95zplus_android_dtb_dump.dts)
- 最最重要的是要修改h618-build的VERSION文件，把里面的24.5.0-trunk修改为最新的文件系统版本，20241012最新为24.11.0-trunk
- 必须使用`非root用户`执行`build.sh`脚本，选择型号开始编译。
- 修改kernel config增加AIC8800 WIFI驱动支持  -> Device Drivers   -> Network device support (NETDEVICES [=y])  -> Wireless LAN (WLAN [=y])    -> AIC wireless Support (AIC_WLAN_SUPPORT [=y])    -> AIC8800 bluetooth Support (AIC8800_BTLPM_SUPPORT [=y])
- 第一次编译通常耗时较长，需要耐心等待。



# 参考 & 感谢

https://github.com/NickAlilovic/build.git

https://github.com/cm9vdA/build-armbian.git

