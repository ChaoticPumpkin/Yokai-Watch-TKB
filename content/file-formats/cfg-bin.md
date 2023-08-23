---
title: ".cfg.bin"
date: 2023-02-05T16:32:00-08:00
draft: false
---

| Magic Number (ASCII) | Magic Number (HEX) | File Type |
|----------------------|--------------------|-----------|
| N/A                  | N/A                | Data      |

A binary file format for storing data. It is used for NPC/menu dialogue, items at stores, objects on the map, etc. It is the binary form of `.cfg` files, although leftover files show that they have a few different extensions, including `.ptree` and `.mapenv`.

For just editing dialogue, [Kuriimu](https://github.com/IcySon55/Kuriimu) works well. If you need to edit other types of the format, Tinifan's [CfgBinEditor](https://github.com/Tiniifan/CfgBinEditor) or a hex editor will work.

## File Information

First off, the `cfg.bin` format supports 4 data types, explained in the below chart.
| Type   | No. of Bytes | Info                            | Example                  |
|--------|--------------|---------------------------------|--------------------------|
| Int    | 4            | 32-bit Integer                  | `0x00000001` (1)         |
| Float  | 4            | Single-precision floating-point | `0x3F800000` (1.0)       |
| Byte   | 1            | 8-bit Integer                   | `0x01` (1)               |
| String | 4            | Pointer to string               | `0x00000001` (See Below) |

The `string` type just references where the string is in the index, while the actual text will be further down in the file. 

## File Segments

The `.cfg.bin` file format is divided in to 4 parts. 

{{< hint type=note >}}
Unfinished Section
{{</hint>}}

## Sources
[Level 5 Bin Files Explained - 	CfgBinEditor](https://github.com/Tiniifan/CfgBinEditor/blob/main/CfgBinEditorExplained.md)