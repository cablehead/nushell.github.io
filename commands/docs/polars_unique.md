---
title: polars unique
categories: |
  dataframe or lazyframe
version: 0.94.0
dataframe_or_lazyframe: |
  Returns unique values from a dataframe.
usage: |
  Returns unique values from a dataframe.
feature: default
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars unique` for [dataframe or lazyframe](/commands/categories/dataframe or lazyframe.md)

<div class='command-title'>Returns unique values from a dataframe.</div>

## Signature

```> polars unique {flags} ```

## Flags

 -  `--subset, -s {any}`: Subset of column(s) to use to maintain rows (lazy df)
 -  `--last, -l`: Keeps last unique value. Default keeps first value (lazy df)
 -  `--maintain-order, -k`: Keep the same order as the original DataFrame (lazy df)


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Returns unique values from a series
```nu
> [2 2 2 2 2] | polars into-df | polars unique
╭───┬───╮
│ # │ 0 │
├───┼───┤
│ 0 │ 2 │
╰───┴───╯

```

Returns unique values in a subset of lazyframe columns
```nu
> [[a b c]; [1 2 1] [2 2 2] [3 2 1]] | polars into-lazy | polars unique --subset [b c] | polars collect
╭───┬───┬───┬───╮
│ # │ a │ b │ c │
├───┼───┼───┼───┤
│ 0 │ 1 │ 2 │ 1 │
│ 1 │ 2 │ 2 │ 2 │
╰───┴───┴───┴───╯

```

Returns unique values in a subset of lazyframe columns
```nu
> [[a b c]; [1 2 1] [2 2 2] [3 2 1]]
    | polars into-lazy
    | polars unique --subset [b c] --last
    | polars collect
╭───┬───┬───┬───╮
│ # │ a │ b │ c │
├───┼───┼───┼───┤
│ 0 │ 2 │ 2 │ 2 │
│ 1 │ 3 │ 2 │ 1 │
╰───┴───┴───┴───╯

```

Creates a is unique expression from a column
```nu
> col a | unique

```