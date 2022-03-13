# XNA Apps
Before the OpenZDK was released it was only possible to build apps using the XNA Framework. These apps use the .NET Compact Framework and the XNA Framework to run. The .NET Compact Framework is a tiny subset of the .NET framework and doesn't even know about the OS it is running on. 

## Files
XNA Apps run in their own [[ZCP Files|ZCP]] container, and can only access data from their own container. This access restriction is only imposed by the XNA Framework/.NET Framework, as [[🗺️ OpenZDK]] apps have access to more files. Although they still can't access any system files. By default two containers are mounted:

- ``gamert``: Hosts all the XNA Runtime libraries 
- ``gametitle``: Hosts the content of XNA application

The path where the content is accessible seems to be: ``\gametitle\584E07D1\Content``. 

XNA Apps can also open other Storage Containers, which are usually used for save files. These containers are accessible through the ``GamerServices``. Using these you can "show" the user a device selector, where in theory they could select the drive they would like to store their save files to. On the Zune this does nothing, but is still needed in order to gain access to such a storage container. The XNA Framework was mainly developed for the XBOX. This is why that weird step is needed. 

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
[[🗺️ XNA Framework]]
