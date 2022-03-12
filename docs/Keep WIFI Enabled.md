# Keep WIFI Enabled
NOTE: This is just some research


## Keep WIFI enabled on WM5 Devices
```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Power\State\Suspend\{98C5250D-C29A-4985-AE5F-AFE5367E5006}  
-change (Default) DWORD Dec to 1  
  
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Power\State\Resuming\{98C5250D-C29A-4985-AE5F-AFE5367E5006}  
-change (Default) DWORD Dec to 1  
  
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Power\State\Unattended\{98C5250D-C29A-4985-AE5F-AFE5367E5006}  
-change (Default) DWORD Dec to 1
```


---
[[Windows CE 6.0]]
