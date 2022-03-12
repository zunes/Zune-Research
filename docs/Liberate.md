# Liberate
Liberate is a application developed by ``Netrix`` which makes it possible to use the ``explorer.exe`` on your Zune. It also provides functionality to run OpenGL, DirectX and Windows Apps on Liberate. 

## WIFI Problem
The Zune automatically disables its WIFI connection after a few minutes to save battery. This is a huge problem when trying to run the Windows CE Remote debugging tools through Liberate for example. 

Liberate actually implemented a somewhat working fix in ``RelayInput.exe``, which just pings google.com and yahoo.com every couple of mins. Unfortunately this fix never starts as Liberate checks ``ZDKCloud_IsConnected()`` to see if it can reach the Zune cloud. Which nowadays always returns ``FALSE`` as the Zune Cloud does not exist anymore. 

I am currently [[Keep WIFI Enabled|looking for a way]] to really fix this.

---
[[OpenZDK]]