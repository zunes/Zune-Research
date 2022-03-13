# zdkimage.h

```c
HRESULT WINAPI ZDKImage_CreateImageFromBuffer(const void *buffer, DWORD length, HIMAGE *image);
HRESULT WINAPI ZDKImage_CreateImageFromFile(LPCWSTR path, HIMAGE *image);
HRESULT WINAPI ZDKImage_GetImageData(HIMAGE image, void *buffer, DWORD length);
HRESULT WINAPI ZDKImage_GetImageSize(HIMAGE image, DWORD *width, DWORD *height);
HRESULT WINAPI ZDKImage_ReleaseImage(HIMAGE image);

DECLARE_HANDLE(HIMAGE);
```


---
[[OpenZDK Reference]]