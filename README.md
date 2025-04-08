<p align="center">
  <img src="https://github.com/CinemaMod/mcef/assets/30220598/938896d7-2589-49df-8f82-29266c64dfb7" alt="MCEF Logo" style="width:66px;height:66px;">
</p>

# MCEF (Minecraft Chromium Embedded Framework)
MCEF is a mod and library for adding the Chromium web browser into Minecraft.

MCEF is based on java-cef (Java Chromium Embedded Framework), which is based on CEF (Chromium Embedded Framework), which is based on Chromium. It was originally created by montoyo. It was rewritten and currently maintained by the CinemaMod Group.

Current Chromium version: `126.0.6478.183`

## Supported Platforms
- Windows 10/11 (x86_64, arm64)*
- macOS 11 or greater (Intel, Apple Silicon)
- GNU Linux glibc 2.31 or greater (x86_64, arm64)**

*Some antivirus software may prevent MCEF from initializing. You may have to disable your antivirus or whitelist the mod files for MCEF to work properly.

**This mod will not work on Android.

## For Modders
MCEF is LGPL, as long as your project doesn't modify or include MCEF source code, you can choose a different license. Read the full license in the LICENSE file in this directory.

### Using MCEF in Your Project
Compile It :D

### Building & Modifying MCEF
After cloning this repo, you'll need to clone the `java-cef` repository (https://github.com/CinemaMod/java-cef/tree/6478) into a separate folder.  
Build it using Python 3.7.9 (this version is required) and Visual Studio 2022.

To correctly compile `java-cef`, follow the official build guide here:  
https://bitbucket.org/chromiumembedded/java-cef/wiki/BranchesAndBuilding.md

Once compiled, copy the `java` folder from the build output into MCEF's `java-cef` submodule folder — do not use the original git submodule version, use the one you just compiled instead.

Next, update the `download-mirror` to point to your own compiled binaries.

And that’s it! If anything is unclear or you'd like a more detailed explanation, feel free to ask and I’ll be happy to clarify.