---
title: from msgpackz
categories: |
  formats
version: 0.94.0
formats: |
  Convert brotli-compressed MessagePack data into Nu values.
usage: |
  Convert brotli-compressed MessagePack data into Nu values.
feature: default
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `from msgpackz` for [formats](/commands/categories/formats.md)

<div class='command-title'>Convert brotli-compressed MessagePack data into Nu values.</div>

## Signature

```> from msgpackz {flags} ```

## Flags

 -  `--objects, -`: Read multiple objects from input


## Input/output types:

| input  | output |
| ------ | ------ |
| binary | any    |

## Notes
This is the format used by the plugin registry file ($nu.plugin-path).