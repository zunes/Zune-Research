# Activating VS 2008 Professional

1. Download [WinSpy - Catch22](https://www.catch22.net/software/winspy)
	1. Run as Admin
2. Goto Control Panel -> Uninstall a Program
	1. Search for Microsoft Visual Studio 2008 Professional Edition
	2. Right Click and then click ``Uninstall/Change``
3.  Click next after loading finishes
4. Use ``WinSpy`` to make the activation boxes visible
	1. Drag the finder tool to one of the hidden controls of the Maintenance Window
	2. In ``WinSpy`` go to the ``Styles`` tab
	3. Click the three dots next to ``Window Styles``
	4. Remove ``WS_DISABLED``
	5. Add ``WS_VISIBLE``
	6. Click Apply
	7. Repeat for the remaining controls 
8. Enter a licence key (can be found online)
9. Click Upgrade

 After step 4 the window should look like this:
 ![[Pasted image 20220720212324.png]]

## References 
- [Upgrading Visual Studio 2008 from trial to full on Windows 7 Beta (Build 7000) - Stack Overflow](https://stackoverflow.com/questions/453262/upgrading-visual-studio-2008-from-trial-to-full-on-windows-7-beta-build-7000)

---
[[🗺️ OpenZDK]]