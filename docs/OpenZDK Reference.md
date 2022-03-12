# Open ZDK Reference
**NOTE: THIS FILE IS STILL WORK IN PROGRESS**

Here is a list of all the OpenZDK libraries and their function signatures. Note that not all of the function signatures have been reverse engineered by the original team.

Also make sure to either define ``ZUNE_HD`` or ``ZUNE_SD`` (for all other models) before compiling your project. 

## zdk.h
This file just includes all other zune header files.

## zcontent.h (SD Only)
**DLL File:** ``zdksystem.dll``
**Coverage:** 3/8 

Function Signatures
```c
HRESULT WINAPI ZContent_Mount(LPCWSTR mountPoint, LPCWSTR container, ZCONTENT_MOUNT_FLAGS flags);
HRESULT WINAPI ZContent_Unmount(LPCWSTR mountPoint);
HRESULT WINAPI ZContent_UnmountAll();
ZContent_Create 
ZContent_Flush 
ZContent_GetInfo 
ZContent_SetMetaData 
ZContent_SetThumbnail 
```

Structures
```c
typedef enum {
	MOUNT_UNKNOWN_1 = 0x1,
	MOUNT_UNKNOWN_2 = 0x2,
	MOUNT_UNKNOWN_4 = 0x4
} ZCONTENT_MOUNT_FLAGS;
```

---
[[OpenZDK]]