---
title: "CTRPluginFramework"
date: 2023-10-30T15:45:11-07:00
draft: false
---

CTRPluginFramework (CTRPF) is a framework for programmatically modding 3DS games. While it is mainly intended to be used as a template for developers to make mod menus and such, it has some very useful memory hacking features on its own. CTRPF can run on both real hardware and through emulation.

## Installation (3DS)

1. Make sure you have the latest [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest)

2. Download the `.3gx` file from the [CTRPF releases](https://github.com/PabloMK7/CTRPluginFramework-BlankTemplate/releases/latest).

3. Rename the file to `default.3gx`, and move it to `SD:/luma/plugins/default.3gx`.

## Installation (Citra)

1. Make sure you have the latest version of [Citra](https://citra-emu.org/).

2. Download the `.3gx` file from the [CTRPF releases](https://github.com/PabloMK7/CTRPluginFramework-BlankTemplate/releases/latest).

3. Rename the file to `default.3gx`, and move it to `/sdmc/luma/plugins/default.3gx` inside Citra's [User Directory](https://citra-emu.org/wiki/user-directory/).

4. Open Citra's settings and check `System > Enable 3GX plugin loader`.

## Basic Usage

Launch a game, you should see the top screen flash blue for a second, followed shortly by a message saying `Plugin Ready!`. You should now be able to press `Select` to open CTRPF's main menu. There are six buttons on the bottom screen, but there's only really two that will be useful to us.

### Action Replay

This is the Action Replay cheats menu. Similar to what Luma3DS has built in, but with greater code support, folders, and a full cheats editor. CTRPF also uses the same cheats directory as Luma, so if you already have cheats for a game, they should show up automatically. Since CTRPF has support for some code types that Luma does not, it's generally advisable to use CTRPF if you're not sure.

Code editing will not be covered in this guide as it is fairly complex, but will be put into its own guide later.

### Search

This is CTRPF's most powerful feature, a memory searcher similar to Cheat Engine or the various old 'game trainer' cheat devices. The basic idea is:

1. You have some value you want to change, for example, your money.

2. You input the value into the search field, and get every match found.

3. You modify the value slightly, then search again.

4. Repeat until there is only one/a few memory addresses to try.

5. Modify to desired value.

This is obviously a simplification, especially for values that are not directly shown to the player, but even this method is enough to modify some parts of the Yo-kai Watch games, like currency value or item quantity.

## Further Reading

Very useful for both understanding other codes and writing your own. - [Action Replay Code Types Supported by CTRPluginFramework](https://gist.github.com/Nanquitas/d6c920a59c757cf7917c2bffa76de860)
