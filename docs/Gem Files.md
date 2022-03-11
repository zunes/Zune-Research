# Gem Files
Gem Files are essentialy ``.XZP`` files (from XBOX) and are defining the UI layout of the Zune. They contain the resources like images, layouts, controls, localisation data, and so on. They are created using the Xbox UI Tool which is part of the XBOX SDK.  

Gem/XZP Files can be unpacked, and contain ``.XUI``, ``.XUR`` and ``.XUS`` files.
A Tool called ``XUIWorkshop`` was used to edit later versions of the file used by the XBOX. The expected version (found in the header of the file) is ``8`` but the Zune's gem files are at Version ``5``. 

The official tool (``XUITool``) to edit the UI was shipped with the XBOX SDK. 

## Tools
- [[Tools/XzpTool 2.exe]]: Can be used to extract the files.

---
[[File Types]]