# Asus-R414-Hackintosh-10.15.7
This EFI can make Asus R414 run MacOS 10.15.7
# How to Use
1、Replace CLOVER in your  EFI folder  
2、This EFI use with Clover R5112，so if you want to make sure that it work normally，please also replace the Boot file and the CLOVER.efi when you replace the file

# What Can‘t Work
1、HD620,it only has 1536MB   
2、Power management，after sleep it can't wake up, so please turn off hibernation and keep the habit of opening and closing the C side    
3、Sound card,it only work on the headset，the speaker can not work because when the system start,the CLOVER  will automatically add a few more parameters, including Layout ID, and it will be automatically generated again after modification，you can find them on CLOVER-OPTIONS-Args,the file have make right layout-id,so if you solve this,it will work normally.  

# Notice

Nerver use Hackintoll ,kext utilys or other tools to rebuild kexts caches ,it will make this reboot always。If you add new kext in CLOVER，it will automatically work after reboot by the configuration in config file,so don't try to rebuild kexts

#Thanks 
This is improved on the basis of   
https://github.com/srole-xiaoxian/ASUS-R414U-Clover  
Thanks to the original author
