# zdkfont.h

```c
typedef enum {
	FONT_STYLE_ITALIC = 2,
	FONT_STYLE_BOLD = 4
} ZDK_FONT_STYLE;

HRESULT WINAPI ZDKFont_Cleanup();
HRESULT WINAPI ZDKFont_Create(LPCWSTR typeface, float size, ZDK_FONT_STYLE style, HGDIOBJ *font);
HRESULT WINAPI ZDKFont_Destroy(HGDIOBJ font);
HRESULT WINAPI ZDKFont_Initialize();
/* ZDKFont_DrawCharToBuffer */
/* ZDKFont_GetCharMetrics */
/* ZDKFont_GetFontMetrics */
```

---
[[OpenZDK Reference]]
