# Koopatlas for Spooky Adventure

Now presenting... Koopatlas! A special version for the Spooky Adventure mod.

Or... Spookatlas. Just kidding, too many people have used the "-atlas" naming scheme. This isn't even that different compared to
Koopatlas, all it has is some fixes and tweaks.

This is based on RoadrunnerWMC's [Koopatlas-Updated][kp-upd], a fork of the original editor. The fork aims to keep it compatible with the latest versions of its dependencies, and to fix bugs and make minor improvements.

## Why?

You may be wondering, why does this exist? Well, it turns out that the path to the folder cotaining NewerSMBW's map tilesets is stored directly inside the KPBIN file. That's right, the filepath isn't in Newer's source code, it's inside the map file for some reason. Spooky Adventure uses a different folder for the world map stuff, therefore, a different folder for the world map tilesets. Which means that the game will fail to load tilesets unless they are present at `/Maps/Texture`.

This version will also fix some tiny little bugs that I've found annoying, mainly just windows not being titled correctly, and other stuff as well.

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
