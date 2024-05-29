---
title: polars uppercase
categories: |
  dataframe
version: 0.94.0
dataframe: |
  Uppercase the strings in the column.
usage: |
  Uppercase the strings in the column.
feature: default
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars uppercase` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Uppercase the strings in the column.</div>

## Signature

```> polars uppercase {flags} ```


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Modifies strings to uppercase
```nu
> [Abc aBc abC] | polars into-df | polars uppercase
╭───┬─────╮
│ # │  0  │
├───┼─────┤
│ 0 │ ABC │
│ 1 │ ABC │
│ 2 │ ABC │
╰───┴─────╯

```