# Keep WIFI Enabled
NOTE: This is just some research


## Interesting entry on Zune Boards
[WLAN Timeout Hack - Zune Boards](https://web.archive.org/web/20170511111746/http://zuneboards.com/forums/showthread.php?t=57096)

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
[[🗺️ Windows CE 6.0]]
