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
  
  # 备注
  如果显示俄语请在oc界面选择reset nvram在重新进行安装即可
  
  
  # 特别感谢 
  iok （https://www.iokiok.tk/2019/01/22/dell-optiplex-5060%E5%AE%89%E8%A3%85%E9%BB%91%E8%8B%B9%E6%9E%9C%E6%89%8B%E8%AE%B0/)
  
  lxyoucan （https://blog.csdn.net/lxyoucan/article/details/110730680）
  
  两位大佬的帖子参考了一整晚才搞定
  
  
