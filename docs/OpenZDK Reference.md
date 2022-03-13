# Open ZDK Reference
Here is a list of all the OpenZDK libraries (this list it not done yet) and their function signatures. Note that not all of the function signatures have been reverse engineered by the original team. Also make sure to either define ``ZUNE_HD`` or ``ZUNE_SD`` (for all other models) before compiling your project. 

**Note:** Function signatures that are commented out have not yet been reverse engineered.

**Note:** ``zdkgl.h`` (use the Tegra headers instead), ``zdkcloud.h`` (Zune Cloud does not exist anymore), ``zcontent.h`` have been omitted, as they don't provide any useable functionality nowadays. 

## zdk.h
This file just includes all other ZDK header files.

## [[zdkaudio.h]]
- **DLL:** zdksystem.dll
- **Coverage:** 16 / 16
- **Description:** Play audio on the Zune.

## [[zdkcontent.h]]
- **DLL:** zdksystem.dll
- **Coverage:** 4 / 7
- **Description:** Open XNA Storage Containers / [[ZCP Files]]

## [[zdkdisplay.h]]
- **DLL:** zdksystem.dll
- **Coverage:** 22 / 23
- **Description:** Functionality for 2D rendering (with DirectX or DirectDraw??)

## [[zdkfont.h]]
- **DLL:** ???
- **Coverage:** 7 / 8
- **Description:** Text Rendering

## [[zdkimage.h]]
- **DLL:** ???
- **Coverage:** ???
- **Description:** Image Loading/Processing

## [[zdkinput.h]]
- **DLL:** ???
- **Coverage:** ???
- **Description:** Get touch and accelerometer data

---
[[🗺️ OpenZDK]]