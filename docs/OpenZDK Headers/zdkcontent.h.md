# zdkcontent.h

```c
/* Container Management */
HRESULT WINAPI ZDKContent_Create(ZDK_CONTAINER_INFO *info, int w, int x, int y, int z);
HRESULT WINAPI ZDKContent_Mount(LPCWSTR mountPoint, ZDK_CONTAINER_INFO *info, BOOL flag);
HRESULT WINAPI ZDKContent_Unmount(LPCWSTR mountPoint);
HRESULT WINAPI ZDKContent_UnmountAll();

/* ZDKContent_Delete */
/* ZDKContent_Flush */
/* ZDKContent_SetMetaData */
/* ZDKContent_SetThumbnail */
/* ZDKContent_FindClose */
/* ZDKContent_FindFirst */
/* ZDKContent_FindNext */

/* Types */
typedef enum {
 CONTAINER_TYPE_RUNTIME = 0x1,
 CONTAINER_TYPE_APPLICATION = 0x2,
 CONTAINER_TYPE_STORAGE = 0x3
} ZDK_CONTAINER_TYPE;

  

typedef struct {
 GUID UserGuid;
 GUID VirtualTitleId;
 ZDK_CONTAINER_TYPE ContainerType;
 wchar_t Name[40];
} ZDK_CONTAINER_INFO;
```

---
[[OpenZDK Reference]]