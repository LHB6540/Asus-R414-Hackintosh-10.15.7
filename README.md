# Asus-R414-黑苹果-10.15.7
这个EFI引导能够使得华硕R414U运行MacOS 10.15.7  

# 如何使用
1、获取黑果小兵网站的10.15.7镜像并制作启动盘  
2、将本项目的EFI文件夹替换U盘的EFI，包括EFI和BOOT文件夹   

# 哪些不能正常
1、HD620集成显卡，仅显示1536MB显存   
2、电源管理的休眠功能不能正常唤醒，请在系统偏好设置中关闭休眠，养成开合C面的习惯以节省电量  
3、声卡，需要注意的是，安装完成后，系统nvram中会自动多出几个引导参数（可能与镜像有关），这会覆盖Clover的引导参数，刚好其中包含了layout-id=7，这不是正确的仿冒ID。这回导致耳机能正常工作而扬声器不能正常工作。如果想解决这个问题，使用终端命令sudo nvram boot-arvg=""清空引导参数重启即可。下次启动时，系统会应用Clover中的layout-id=21，尽管它能使扬声器和耳机同时工作，但也并不是完美的，在使用耳机时需要在系统偏好设置-声音中将声道调整为左声道或者右声道，否则声音会有异常，幸运的是，你只需要设置一次即可，而且不会影响到扬声器的声效。 



# Asus-R414-Hackintosh-10.15.7
This EFI can make Asus R414 run MacOS 10.15.7
# How to Use
1、Replace CLOVER in your  EFI folder  
2、This EFI use with Clover R5112，so if you want to make sure that it work normally，please also replace the Boot file and the CLOVER.efi when you replace the file

# What Can‘t Work
1、HD620,it only has 1536MB   
2、Power management，after sleep it can't wake up, so please turn off hibernation and keep the habit of opening and closing the C side    
3、Sound card,it only work on the headset，the speaker can not work because when the system start,the CLOVER  will automatically add a few more parameters, including Layout ID, and it will be automatically generated again after modification，you can find them on CLOVER-OPTIONS-Args.If your want to slove it

# Notice

Nerver use Hackintoll ,kext utilys or other tools to rebuild kexts caches ,it will make this reboot always。If you add new kext in CLOVER，it will automatically work after reboot by the configuration in config file,so don't try to rebuild kexts

#Thanks 
This is improved on the basis of   
https://github.com/srole-xiaoxian/ASUS-R414U-Clover  
Thanks to the original author
