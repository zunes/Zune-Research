# OpenZDK Setup
This step by step guide will show you how to install all the tools needed to develop OpenZDK Apps on Windows 10. Make sure to follow all the steps in the right order.

**Note:** Installing the actual OpenZDK is only necessary if you want to develop applications or use tooling associated with it.

- You can download all the installers (except Visual Studio 2008) from [here](https://www.mediafire.com/file/zshfm8ocyskzm4u/Installers.zip/file).
- Visual Studio 2008 Pro (90 day trial) can be downloaded from Microsoft [here](https://download.microsoft.com/download/8/1/d/81d3f35e-fa03-485b-953b-ff952e402520/VS2008ProEdition90dayTrialENUX1435622.iso).

## Installing prerequisites
1. Install ``Visual Studio 2008`` Professional
	
	Make sure to select  ``Smart Device Programmability`` when installing. This is only available in the Pro versions of Visual studio.
	
3. (Optional) Install ``Visual Studio 2008 SP1``
2. Install ``XNA Game Studio 3.1`` (``XNAGS31_setup.exe``)
	
	On Windows 10 this needs some extra steps as the installer is broken. Thanks to [this](https://www.reddit.com/r/Zune/comments/m5yx74/finally_got_xna_31_studio_running/) Reddit Post for elaborating how to extract the installer:
	
	1. Open a **Command Prompt** and navigate to the directory of the installer
	2. Run the installer with the ``/x`` option like this: ``XNA3.1.exe /x``
	3. Run every **MSI** installer you see that got extracted
	4. Run everything in ``C:\Program Files (x86)\Microsoft XNA\XNA Game Studio\v3.1\Setup``
	
3. Install ``Zune HD extensions for XNA Game Studio.msi``

## Setup your Zune in XNA Game Studio
1. Plug in your Zune and make sure that the **Zune Software** is completely closed.
2. Open ``XNA Game Studio Device Center`` which is located at ``C:\Program Files (x86)\Common Files\Microsoft Shared\XNA\Device Center``
3. Click **Add Device**, then **Zune**
4. Select your Zune and continue through the remaining steps


## Install OpenZDK
1. Close all instances of Visual Studio
2. Install the ``OpenZDK`` (``openzdk-hd-4.5-20100414.msi``), can be found in the **Quick Start Kit**
3. Select **Custom** installation type
4. Set **Documentation** to **Entire feature will be unavailable** - The docs are only available if you have Visual Studio 2005 installed, and don't provide any OpenZDK specific information anyways
5. Continue through the remaining steps

## Install the Platform Support Pack (for OpenGL)
1. Install ``Standard SDK for Windows CE 5.0``  (``STANDARD_SDK.msi``): The Nvidia installer needs this to finish installing
2. Install ``NVIDIA Tegra 250 Platform Support Pack`` (``ce6_tegra_250_5265393.msi``): This contains all the library needed to use the NVIDIA hardware

## Setting up Visual Studio for development
1. Updating the include path
	1. In Visual Studio select **Options > Tools > Projects and Solutions > VC++ Directories**
	2. Select **OpenZDK (ARMV4I)** from the **Platform** dropdown
	3. Select **Include files** from the **Show directories for** dropdown
	4. Click the **New line** button
	5. Enter ``$(NV_WINCE_T2_PLAT)\include`` and press enter
2. Updating the library path
	1. Select **Library files** from the **Show directories for** dropdown
	2. Click the **New line** button
	3. Enter ``$(NV_WINCE_T2_PLAT)\lib\release`` and press enter


**That's it! Have fun developing :)**

Check out the [[🗺️ Official Documentation]] or [[OpenZDK Reference]] for more information about the available APIs.

To activate VS 2008 [[Activating Visual Studio 2008 Profressional|look here]].

## References
- [Reddit - Finally got XNA 3.1 studio running](https://www.reddit.com/r/Zune/comments/m5yx74/finally_got_xna_31_studio_running/)
- [ZuneDevWiki - Installing prerequisites](https://web.archive.org/web/20100526061444/http://zunedevwiki.org/wiki/getting_started/developer/prerequisites)
- [ZuneDevWiki - Preparing the Zune development environment](https://web.archive.org/web/20100701170332/http://zunedevwiki.org/wiki/getting_started/developer/openzdk)

---
[[🗺️ OpenZDK]]