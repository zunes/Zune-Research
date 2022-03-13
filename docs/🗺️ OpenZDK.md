# 🗺️ OpenZDK
The OpenZDK is a SDK for writing applications for the Zune and was developed by people going by the usernames ``itsnotabigtruck``, ``Netrix`` and ``Nurta``. In contrary to the XNA Framework, the OpenZDK allows far more control over the Zune's hardware, like access to [[🗺️ OpenGL ES]] and other useful libraries. 

The OpenZDK works by using a bug in the Shell which allows it to execute arbitrary code outside of the very limited .NET Compact Framework. This code still runs in user mode, and not with elevated privileges. The original authors have created **header** and **library** files from Zune specific DLLs like ``zdksystem.dll`` by reverse engineering their function signatures, in order to get access to the Zune's API.

Most of the documentation can be access on ``zunedevwiki.org`` (use webarchive). I will try to add as much information as possible over time, as the webarchive is painfully slow.

## Topics
- [[OpenZDK Setup]]
- [[OpenZDK Reference]]

## Apps
- [[Liberate]]

## References
- [Reddit - Finally got XNA 3.1 studio running](https://www.reddit.com/r/Zune/comments/m5yx74/finally_got_xna_31_studio_running/)
- [Zune Dev Wiki (through web.archive.org)](https://web.archive.org/web/20100526061444/http://zunedevwiki.org/wiki/getting_started/developer/prerequisites)
- [Reddit - Play Gameboy games on your Zune HD](https://www.reddit.com/r/Zune/comments/c38f7/play_gameboy_games_on_your_zune_hd/)

