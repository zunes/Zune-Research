# zdkdisplay.h

```c
/* 2D initialization */
HRESULT WINAPI ZDKDisplay_Initialize();
HRESULT WINAPI ZDKDisplay_Cleanup();

  

/* System information */
HRESULT WINAPI ZDKDisplay_GetInfo(DWORD *screenWidth, DWORD *screenHeight);

  

/* Texture management */
HRESULT WINAPI ZDKDisplay_CreateTexture(DWORD width, DWORD height, HTEXTURE *texture);
HRESULT WINAPI ZDKDisplay_FreeTexture(HTEXTURE texture);
HRESULT WINAPI ZDKDisplay_GetTextureData(HTEXTURE texture, ZDK_RECT *rect, void *buffer, DWORD dataSize);
HRESULT WINAPI ZDKDisplay_GetTextureInfo(HTEXTURE texture, DWORD *width, DWORD *height);
HRESULT WINAPI ZDKDisplay_SetTextureData(HTEXTURE texture, ZDK_RECT *rect, void *buffer, DWORD dataSize);
HRESULT WINAPI ZDKDisplay_TextureLockRect(HTEXTURE texture, ZDK_TEXTURE_LOCK_INFO *info, ZDK_RECT *rect, ZDK_TEXTURE_LOCK_FLAGS flags);
HRESULT WINAPI ZDKDisplay_TextureUnlockRect(HTEXTURE texture);

/* Rendering */
HRESULT WINAPI ZDKDisplay_BeginScene();
HRESULT WINAPI ZDKDisplay_Clear(DWORD color);
HRESULT WINAPI ZDKDisplay_DrawSprites(ZDK_SPRITE *sprites, DWORD spriteCount);
HRESULT WINAPI ZDKDisplay_EndScene();
HRESULT WINAPI ZDKDisplay_Present();
HRESULT WINAPI ZDKDisplay_ResolveBackBuffer(HTEXTURE texture);
HRESULT WINAPI ZDKDisplay_SetBlendMode(ZDK_BLEND_MODE blendMode);
HRESULT WINAPI ZDKDisplay_SetClipRect(ZDK_RECT *rect);
HRESULT WINAPI ZDKDisplay_SetRenderTarget(HTEXTURE texture);
HRESULT WINAPI ZDKDisplay_SetTexture(HTEXTURE texture);
HRESULT WINAPI ZDKDisplay_SetTransform(ZDK_MATRIX *matrix);
/* ZDKDisplay_SetTextureFilter */


/* Types */
typedef float ZDK_MATRIX[4][4];

typedef struct {
 int Left;
 int Top;
 int Right;
 int Bottom;
} ZDK_RECT;

typedef enum {
 BLEND_MODE_NONE,
 BLEND_MODE_ALPHA_BLEND,
 BLEND_MODE_ADDITIVE
} ZDK_BLEND_MODE;

  

typedef struct {
 float X;
 float Y;
 float U;
 float V;
} ZDK_VERTEXDATA;

  

typedef struct {
 ZDK_VERTEXDATA Vertices[4];
 DWORD Color;
} ZDK_SPRITE;

DECLARE_HANDLE(HTEXTURE);

typedef enum {
	TEXTURE_LOCK_DEFAULT = 0x0,
	TEXTURE_LOCK_READONLY = 0x10,
	TEXTURE_LOCK_NOSYSLOCK = 0x800, /* questionable */
	TEXTURE_LOCK_NOOVERWRITE = 0x1000, /* questionable */
	TEXTURE_LOCK_DISCARD = 0x2000,
	TEXTURE_LOCK_NO_DIRTY_UPDATE = 0x8000 /* questionable */
} ZDK_TEXTURE_LOCK_FLAGS;

typedef struct {
	int Pitch;
	DWORD *Buffer;
} ZDK_TEXTURE_LOCK_INFO;
  
```

---
[[OpenZDK Reference]]