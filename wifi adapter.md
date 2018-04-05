# Installation Adapter 
1. iwlwifi 
2. wdc wifi
3. manual loading wifi
  * show all wifi id
  * connet wifi id

## manual loading wifi 
### show all wifi SSID
```bash
nmcli -p dev wifi
```

### connect wifi SSID
* example : 
```bash
nmcli con up id 'ETG XSIS'
```
