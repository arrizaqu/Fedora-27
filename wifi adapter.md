# Installation Adapter 
1. iwlwifi 
2. wdc wifi
3. manual loading wifi
  * show all wifi id
  * connet wifi id
  * stop wifi 

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
