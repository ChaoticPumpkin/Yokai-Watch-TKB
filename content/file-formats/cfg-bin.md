---
title: ".cfg.bin"
date: 2023-02-05T16:32:00-08:00
draft: false
---

| Magic Number (ASCII) | Magic Number (HEX) | File Type |
|----------------------|--------------------|-----------|
| N/A                  | N/A                | Data      |

A binary file format for storing data. It is used for NPC/menu dialogue, items at stores, objects on the map, etc. It is the binary form of `.cfg` files, although leftover files show that they have a few different extensions, including `.ptree` and `.mapenv`.

For just editing dialogue, [Kuriimu](https://github.com/IcySon55/Kuriimu) works well. If you need to edit other types of the format, use either a hex editor or [CfgBinEditor](https://github.com/togenyan/CfgBinEditor), the latter of which is more user friendly, but requires more setup and is quite incomplete.
