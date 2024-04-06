# Koopatlas for Spooky Adventure

Now presenting... Koopatlas! A special version for the Spooky Adventure mod.

Or... Spookatlas. Just kidding, the "`-atlas`" naming scheme is done-to-death by now, there's at least like 6 or 7 of them by now. This isn't even different enough to get a new "prefix", all it has is some fixes and tweaks.

This is based on RoadrunnerWMC's [Koopatlas-Updated][kp-upd], a fork of the original editor. That fork aims to keep it compatible with the latest versions of its dependencies, and to fix bugs and make minor improvements.

## What's so special about this version?

Well, this version of Koopatlas includes multiple new features that go along with the in-game Koopatlas engine! See below for some new features:

### New Tileset Folder Path
It turns out that the path to the folder containing NewerSMBW's map tilesets is stored directly inside the KPBIN file. That's right, the filepath isn't in Newer's source code, it's inside the map file for some reason.

Spooky Adventure uses a different folder for the world map stuff, therefore, a different folder for the world map tilesets. Which means that the game will fail to load tilesets unless they are present at `/Maps/Texture`.

### New SIGN Node Type
A new feature in Spooky Adventure is signs on the World Map! These nodes have a Message ID option, just set it to whatever the ID is of the message you want to load, and it'll load it from `MapSignMessages.bin` in the `/SpookyRes` folder.

### Miscellaneous Bugfixes
Several minor bugs have been fixed in this version, mainly just visual issues and such:
- Added missing window titles and icons
- Changed some text strings to be more accurate
- On `CHANGE` nodes, the Transition type dropdown was displayed below the Map filepath textbox, making it hard to read. The dropdown now displays above the textbox
- The nonfunctional "Open Recent" option has been removed

## Original readme below

Where do I even begin with this...

This is the editor half of Koopatlas - a totally new 2D map engine we wrote
for Newer. Without going into too much detail, here's a quick roundup:

- Ridiculously buggy and unpolished editor
- 2D maps with an unlimited* amount of layers
- Tileset layers, supporting an unlimited* amount of tilesets
- Doodad layers, allowing you to place arbitrary textures on the map at any
  position and scale/rotate them
- Doodad animations
- Unlockable paths and level nodes
- More hardcoded things than you can shake a stick at (possibly rivalling
  Nintendo's 3D maps)
- Multiple maps with entrances/exits a la Reggie
- Maps are stored in a ".kpmap" format for easy editability - a JSON file in a
  specific format - and exported to an optimised ".kpbin" format for usage
  in-game

*\*Unlimited: Not really. This is the Wii, a game console which was
underpowered when it was released in 2006. There's not a lot of room in RAM
for lots of tilesets and doodads. A couple of the Newer maps use up almost all
the available space, so...*

If you want to make maps, feel free to try it. Then bash your head against a
wall when you accidentally close the editor and lose your unsaved work because
there's no warning against that. Or when it crashes on you, which might happen.

[kp-upd]: https://github.com/RoadrunnerWMC/Koopatlas-Updated
