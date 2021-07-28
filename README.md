# Dell-Optiplex-5060-SFF-OC-EFI
配置信息
CPU:i5-8500

SSD:SN 750 500gb

HDD: WD Blue 500 gb

Graphics Card: R5 430 1gb

# Bios Setting
General
  ->Boot Sequence  勾选所有Boot Sequence选项，Boot List Option勾选UEFI启动
  ->Advanced Boot Options  取消Enable Legacy Option ROMs

System Configuration
  ->Serial Port  勾选Disabled
  ->SATA Operation  勾选AHCI
  ->USB Configuration  勾选全部
  ->Audio  勾选全部

Video
  ->Primary Display  勾选Intel HD Graphics

Secure Boot
  ->Secure Boot Enable  勾选Disable
  ->Secure Boot Mode  勾选Deployed Mode

Intel Software Guard Extensions
  ->Intel SGX Enable  勾选Disable

Virtualization Support
  ->Virtualization  取消勾选Enable Intel Virtualization Technology
  ->VT for Direct I/O  取消勾选Enable VT for Direct I/O
  
  #Knows Issue
  R5 430 1gb cant use on the os
  
  # 修改DVMT以便让4k显示器正常显示
  如果需要更大的核显显存可以下载70yuan.zip里的bootx64.efi并在u盘里创建esp分区>ESP>BOOT>Bootx64.efi把文件拷贝进去
  重启电脑选择u盘启动输入指令
![226127838_489584928690080_8555867824362502745_n](https://user-images.githubusercontent.com/73232581/127264501-df0e62c1-8d32-40e4-b5dc-09a2e755ac8e.jpg)

  setup_var 0x8DC检查显存是不是64M如果是应该显示0x2
  如果显示0x1 就输入指令setup_var 0x8DC 0x2
  后在输入setup_var 0x8DC 以确保显存已经更改
  ![225592232_253543346307178_4912180426199934437_n](https://user-images.githubusercontent.com/73232581/127264530-4bde1f31-24ed-4496-82cf-ca272fa347b1.jpg)

  # 禁用CFG Lock
   和修改DVMT显存步骤一样只不过要输入的指令不同
   setup_var 0x5BE 0x0   （禁用CFG lock）
  ![224280584_184479503734939_553406311726663015_n](https://user-images.githubusercontent.com/73232581/127264739-49cc6501-c0ad-436d-8c91-18735904cd10.jpg)

  # 备注
  如果显示俄语请在oc界面选择reset nvram在重新进行安装即可
  
  
  # 特别感谢 
  iok （https://www.iokiok.tk/2019/01/22/dell-optiplex-5060%E5%AE%89%E8%A3%85%E9%BB%91%E8%8B%B9%E6%9E%9C%E6%89%8B%E8%AE%B0/)
  
  lxyoucan （https://blog.csdn.net/lxyoucan/article/details/110730680）
 Chamsiinlong （https://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1820336）![Uploading 224280584_184479503734939_553406311726663015_n.jpg…]()

  
  两位大佬的帖子参考了一整晚才搞定
  
  
