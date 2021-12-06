# MSI B460M EFI iGPU 黑苹果 Hackintosh
> 能帮到别人真的很开心。今天2021/12/04将OpenCore更新到最新版0.7.5，支持最新版MacOS12
>
> 增加 <a href="#1">极速安装方法</a> 和  <a href="#2">更新MacOS系统和OpenCore方法</a> 安装和更新的时候就不怕忘记了。

OpenCore 0.7.5 , MacOS Monterey 12.0.1

支持：MSI B460M + 所有10代核显CPU

日期：2021/12/04



## Monterey 12.0.1安装成功

![桌面](https://user-images.githubusercontent.com/13514929/144720887-692f792f-d0d6-49e8-819d-b087ee2598be.png)



## 使用方法

##### ⚠️ 注意 ⚠️ 注意 ⚠️ 注意 

下载后请自行修改 **序列号** 和 **ROM** 防止重复，修改方法 [修改序列号教程](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo)

#### <a name="1">极速安装</a>：

1. 准备4G以上U盘并格式化为FAT32格式
2. 下载文件后解压，将 **EFI** 和 **com.apple.recovery.boot** 文件夹拷贝到U盘根目录
2. 用python执行macrecovery.py下载对应的MacOS恢复镜像，详见**com.apple.recovery.boot**文件夹下的README.md说明
2. 重启 - 选择U盘启动 - Recovery xx.xx.x (dmg)
2. 安装过程，file - 中文，磁盘需要格式为APFS+GUID分区图
6. 安装完成后，复制U盘EFI文件夹到EFI分区
   1. 下载MountEFI https://github.com/corpnewt/MountEFI
   2. 双击 `MountEFI.command` 选择当前磁盘
   3. 复制U盘EFI文件夹到EFI磁盘


#### <a name="2">更新MacOS系统和OpenCore</a>：

在更新系统前，先查看当前OpenCore版本是否支持需要更新的系统，如果不支持就别更新了。

1. 下载最新EFI文件
2. 替换EFI分区的EFI文件夹
   1. 下载MountEFI https://github.com/corpnewt/MountEFI
   2. 双击 `MountEFI.command` 选择当前磁盘
   3. 复制EFI文件夹到EFI磁盘
3. 系统升级：系统偏好设置 - 系统更新 - 安装更新

#### 其他情况：

- 添加Win引导（如果Win引导丢失）
  1. 通过U盘启动window安装程序
  2. 在选择语界面，按Shift + F10 运行命令提示符，输入：`bcdboot C:\Windows /l zh-cn`
    
- 设置默认启动系统

  在系统选择界面，按control + 数字

## 硬件配置

主板：微星B460M迫击炮 

CPU：英特尔 i5 10500

GPU：核显 UHD 630 

网卡：板载网卡 Realtek® RTL8125B 2.5G LAN

声卡：板载声卡 Realtek® ALC1200

硬盘：西数M.2 WD SN550 500GB  

内存：芝奇 32G （G.SKILL 8GB DDR4 3200 * 4）

WiFi/蓝牙：免驱BCM94360 / 蓝牙4.0





## 检查清单

- [x] 最大分辨率显示 （34英寸3440×1440）
- [x] 硬件解码
- [x] WiFi
- [x] 蓝牙
- [x] 隔空投送
- [x] USB3.0 / 2.0
- [x] 声音/录音
- [x] Xcode
- [x] FCPX
- [x] 双系统切换



Geekbench CPU跑分 https://browser.geekbench.com/v5/cpu/8042171

Geekbench GPU跑分 https://browser.geekbench.com/v5/compute/2870286

