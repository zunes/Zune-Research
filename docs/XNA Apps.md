# XNA Apps
Before the OpenZDK was released it was only possible to build apps using the XNA Framework. These apps use the .NET Compact Framework and the XNA Framework to run. The .NET Compact Framework is a tiny subset of the .NET framework and doesn't even know about the OS it is running on. 

## Files
XNA Apps run in their own container, and can only access data from their own container. 
The default path (from within an XNA App) where the deployed files lie seems to be ``\gametitle\584E07D1\Content``. This path is probably the mount path of the [[ZCP Files|ZCP File]] mounted by ``zcstfs.dll``. This access restriction is only imposed by the XNA Framework/.NET Framework, as [[OpenZDK]] apps have access to more files. Although they still can't access any system files or files like that.  

XNA Apps can also open another Storage Container, which is usually used for a game's save file. These containers are accessible through the ``GamerServices``. Using these you can "show" the user a device selector, where in theory they could select the drive they would like to store their save files to. On the Zune this does nothing, but is still needed in order to gain access to such a storage container. The XNA Framework was mainly developed for the XBOX. This is why that weird step is needed. 

Code Sample:
```c#
IAsyncResult async = Microsoft.Xna.Framework.GamerServices.Guide.BeginShowStorageDeviceSelector(null, null);

var storage = Microsoft.Xna.Framework.GamerServices.Guide.EndShowStorageDeviceSelector(async);
Debug.WriteLine("Is connected: " + storage.IsConnected);
            
var container = storage.OpenContainer("ZuneCraft");
Debug.WriteLine("Container Path: " + container.Path);
```
The file path can be composited using ``container.Path + PATH_TO_YOUR_FILE``.

---
[[XNA Framework]]
