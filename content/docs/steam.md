---
title: Steam
---

# Setup

Environment Variables  
Advanced System Settings (System Properties → Advanced) → Environment Variables

- `GENSO_SMB_HOST` = `smb.gensokyo.zone`
- <span id="env_GENSO_SMB_SHARED_MOUNT"></span>`GENSO_SMB_SHARED_MOUNT` = `\\smb.gensokyo.zone\shared` or `X:` if mapped as a network drive (recommended)
- `GENSO_STEAM_MACHINE` = `mypc` your computer’s name goes here
- <span id="env_GENSO_STEAM_LOCAL_DATA"></span>`GENSO_STEAM_LOCAL_DATA` = `C:\Program Files\GensokyoZone` or somewhere local to be used as scratch space
- <span id="env_GENSO_STEAM_INSTALL"></span>`GENSO_STEAM_INSTALL` = `C:\Program Files (x86)\Steam` or wherever Steam is installed to

## Library

A network share folder is reserved for storing and sharing Steam games.
Add a new library in Steam’s settings to [<span class="pathvalue">%GENSO_SMB_SHARED_MOUNT%\steam\library</span>](#env_GENSO_SMB_SHARED_MOUNT) for access.

# Beat Saber

## Setup

Environment Variables  
- `GENSO_STEAM_LIBRARY_BS` = `G:\SteamLibrary` if Beat Saber is installed to a different disk than [`%GENSO_STEAM_INSTALL%`](#env_GENSO_STEAM_INSTALL)

The scripts to manage the Beat Saber install are found under [<span class="pathvalue">%GENSO_SMB_SHARED_MOUNT%\steam\bin</span>](#env_GENSO_SMB_SHARED_MOUNT).
It is recommended to create a shortcut to this folder for convenient access by holding Alt and dragging it onto your Windows desktop.

To start initial setup, an existing Beat Saber install must be moved to its new home under [<span class="pathvalue">%GENSO_STEAM_LOCAL_DATA%\Beat Saber\Vanilla</span>](#env_GENSO_STEAM_LOCAL_DATA) by running <span class="pathvalue">beatsaber/setup.bat</span>.

``` bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\beatsaber\setup.bat
```

## Updates

It is recommended that the Steam `Automatic Updates` setting is changed to "Only update this game when I launch it" under the game’s right click `Properties` → `Updates` to avoid issues later on.

When Steam does need to update the game, the [vanilla local install](#beatsaber_Vanilla) must be restored for it to successfully perform the update and then allow you to continue playing the game. This just requires running <span class="pathvalue">beatsaber/local-vanilla</span> prior to clicking the "Update" button in Steam.

``` bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\beatsaber\local-vanilla.bat
```

## Play

Before playing the game, you must first select your user and game version:

``` bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\steam\arc.bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\beatsaber\1_34_2.bat
```

These will be saved as environment variables to be used the next time the game is launched.

Now to prepare the game:

``` bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\beatsaber\mount.bat
```

This will set up directory links for the [user and version previously selected](#beatsaber_UserVersion).
The game can now be launched normally through steam.

Alternatively, you can mount and launch the game in one convenient command:

``` bat
%GENSO_SMB_SHARED_MOUNT%\steam\bin\beatsaber\launch.bat
```
