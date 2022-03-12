# ZCP Files
NOTE: This note is still very rough, it just contians some copied info from the xda-froum.

Also of note is how applications function. The leaked WP7 docs note that each app runs in its own “isolated sandbox”. This is how the Zune HD functions as well. Each application is packaged into a “zcp” file which (as someone else in this thread said) seems to be some sort of almost VHD file format. Then when the app loads, it basically mounts that ZCP file and everything runs within that (zctfs.dll). The app is only allowed to read/write to that file. Although it doesn’t seem like XNA game studio apps get packaged into this (unless the Zune builds a new file and packages everything?).

a) .zcp files have nothing to do with Zortech, even though they apparently have the same file extension.  
b) A .zcp file is like a mini-filesystem that can be mounted and accessed on the Zune. They're kinda like .iso images, but writable as well.  
c) Everything in XNA is stored in containers. There's 3 types of containers: game containers, runtime containers, and storage containers. All three are stored on the Zune itself as .zcp files.  
d) Runtime containers include the XNA runtime files and are identified by a particular runtime token.  
e) Game containers store everything deployed along with a game and specify the runtime container needed by the game, which is automatically loaded when the game is started.  
f) Storage containers are what games use for storing data, and have to be manually loaded through code in the game.  
g) The built-in Zune games are both signed and encrypted, making them near-impossible to modify and difficult to even analyze.  
h) The integrated runtime, which is deployed along with the games, is not encrypted, but it is signed. It isn't much different from the ordinary runtime that's deployed automatically along with user-created Zune games.  
i) The built-in games and integrated runtime are not deployed through the same method that user-created games are: they're dumped straight onto the Zune.

---
[[File Types]]
