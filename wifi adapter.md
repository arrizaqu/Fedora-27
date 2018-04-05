# Installation Adapter 
1. iwlwifi 
2. wdc wifi
3. manual loading wifi
  * show all wifi id
  * connet wifi id

## manual loading wifi 
### show all wifi SSID
```command
nmcli -p dev wifi
```

### connect wifi SSID
* example : 
```command
nmcli con up id 'ETG XSIS'
```
