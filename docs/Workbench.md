# Workbench
A place for me to quickly write down found information, will be sorted later.


## Strings contained in various binaries
### zam_srv.dll
This service is responsible for the XNA connection. 

```
Services\ZAM\PowerManagement 
ZamPowerMgr

Interesting looking guids:
{24327589-6EEA-4fb7-B57E-3C8373CC1C46}\DSP1:
{A32942B7-920C-486b-B0E6-92A702A99B35}\ACL1:
{A32942B7-920C-486b-B0E6-92A702A99B35}\CPU1:
{A32942B7-920C-486b-B0E6-92A702A99B35}\ZTP1:


Probably win32 events:
ZAM/Started 
ZAM/AppExitEvent 
Zune/CpuChangeEvent 
ZAM/XnaDbgConnectionClose 
ZAM/XnaDbgConnectionPending 
ZAM/XnaDbgHandlerActive 
ZAM/MESSAGEQUEUE

Some paths:
Update\nk.bin 
Update\ext.bin 
Update\zboot.bin 
Update\recovery.bin 
Update\mtece.bin
```

## Microsoft.Xna.RemoteServices Service IDs
These are services are used by XNA to deploy your app (for eg when making an app in Visual Studio). These are also used by DeployKit.
```
{7F7534A1-293D-495E-88DA-F1EA984EF075} Profiler
{92C8EE24-92DF-4cb5-99C2-B4C7068528E9} Console
{7ABBE0D5-B437-42ca-B57B-CEED61680E4F} Debugger
{2B80CE0A-7119-413e-BA6F-E451AC9382AF} Performance monitor
{754BD393-556F-4a33-8541-BC009FFE979E} Sampling profiler
{D8F4AE7C-581B-4898-97C0-F08EBC001D20} Error popup suppression
{BC66BB72-DE63-4b31-956E-B3878CE9F5D2} Test target
{D0F348D2-9667-4ef2-B078-BF94077177FD} Trace
XnaChannelBroker                       Deployment/launch channel broker
XnaScreenshotService                   Screenshot acquisition
XNACHANx                               Brokered channel (x = returned channel ID)
```
