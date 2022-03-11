# Open ZDK
The Open ZDK is a SDK for writing applications for the Zune and was developed by people going by the usernames ``itsnotabigtruck``, ``Netrix`` and ``Nurta``. In contrary to the XNA Framework, the Open ZDK allows far more control over the Zune's hardware, like access to [[OpenGL ES]] and other useful librarys. 

The OpenZDK works by using a bug in the Shell which allows it to execute arbitrary code outside of the very limited .NET Compact Framework. NOTE: This code still runs in user mode, and not with elevated priveleges.
The original authors have created **header** and **library** files from Zune specific dlls like ``zdksystem.dll`` by reverse engeneering their function signatures, in order to get access to Zune's API.

Most of the documentation can be access on ``zunedevwiki.org`` (use webarchive).

## Setup
[[TODO]]: Write Setup Tutorial

Useful notes to install the XNA framework on windows 10:
1.  basically grab the XNA3.1 install exe
2.  push Windows R to get into run
3.  browse to your EXE
4.  after the last " place /x
5.  "C:/Temp/XNA3.1.exe " /x
6.  this will extract the exe to wherever you chose
7.  Run every MSI you see (redist and then one that starts with an A)
8.  then goto C:\Program Files (x86)\Microsoft XNA\XNA Game Studio\v3.1\Setup
9.  run everything you see in there

## Links
- https://www.reddit.com/r/Zune/comments/m5yx74/finally_got_xna_31_studio_running/
- https://web.archive.org/web/20100526061444/http://zunedevwiki.org/wiki/getting_started/developer/prerequisites
- https://www.reddit.com/r/Zune/comments/c38f7/play_gameboy_games_on_your_zune_hd/

