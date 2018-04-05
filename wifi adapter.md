# Installation Adapter 
1. iwlwifi 
2. WICD wifi
3. manual loading wifi
  * show all wifi id
  * connet wifi id
  * stop wifi 
4. Semi GUI NMTUI

## WICD Wifi
### Intallation 
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

