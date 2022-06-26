---
title: first
version: 0.64.0
usage: |
  Creates new dataframe with first rows
---

# <code>{{ $frontmatter.title }}</code>

<div style='white-space: pre-wrap;'>{{ $frontmatter.usage }}</div>

## Signature

```> first (rows)```

## Parameters

 -  `rows`: Number of rows for head

## Examples

Create new dataframe with head rows
```shell
> [[a b]; [1 2] [3 4]] | to-df | first 1
```