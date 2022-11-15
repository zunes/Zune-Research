# ZCP Files
NOTE: This note is still very rough, it just contains some copied info from the xda-froum.

These files are XNA Storage Containers. They are essentially a mini filesystem in a single file, similar to a VHD for example. They are mounted by the Zune at runtime when launching an [[XNA Apps|XNA Application]]. Each application is packaged into its own ZCP File. 
The filesystem used is called **Zune Content File System** (zcstfs.dll) and is actually registered by the StorageManger in the Registry at ``HKEY_LOCAL_MACHINE\System\StorageManager\ZCSTFS``.

There are 3 different types of Storage Containers used by XNA:
- **Game Containers:**  Mounted automatically at ``/gametitle/`` and stores all the deployed app content.
- **Runtime Containers:** Mounted automatically at ``/gamert/`` and stores all the XNA Runtime libraries.
- **Storage Containers:** Has to be [[XNA Apps#Files|manually loaded]] and will be mounted at ``/xnaa/``. Usually used for save files. 

## Deployment
When deploying an application to the Zune, it will receive all the files from the computer and then package them into a new zcp container. It is mounted during deploy and launch of the title. 

DeployKit uses the same XNA apis as Visual Studio to deploy apps. 

---
[[🗺️ File Types]], [[🗺️ XNA Framework]]
