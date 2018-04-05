# Installation Adapter 
1. iwlwifi 
   * Installation Driver
2. WICD wifi
   * Installation
   * Disable NetworkManager and Enable Wicd
   
3. Manual loading wifi
   * Show all wifi ssid
   * Connet wifi ssid
   * Stop wifi 
4. Semi GUI NMTUI

## IWLWIFI
### Installation Driver
1. https://github.com/torvalds/linux/tree/master/drivers/net/wireless/intel/iwlwifi
2. https://wireless.wiki.kernel.org/en/users/drivers/iwlwifi

## WICD Wifi
### Installation 
```command
yum install wicd wicd-common wicd-gtk
yum remove NetworkManager //optional if you confident nothing error.
```
## Disable NetworkManager and Enable WICD
```command
service NetworkManager stop
service wicd start
```
Search Linux menu 'Wicd Network Manager'

## Manual loading wifi 
### show all wifi SSID
```command
nmcli -p dev wifi
```
or 
```command
nmcli d wifi list
```

### connect wifi SSID
* example : 
```command
nmcli con up id 'ETG XSIS'
```

### stop connection wifi SSID
* example 
```command
nmcli con down id 'ETG XSIS'
```

## Semi GUI NMTUI
```command
nmtui
```

## Contact Email 
arrizaqu@yahoo.com

## Reference 
1. https://ask.fedoraproject.org/en/question/8274/unstable-wireless-connection/
