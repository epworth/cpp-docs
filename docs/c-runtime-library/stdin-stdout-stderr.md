---
description: "Learn more about: stdin, stdout, stderr"
title: "stdin, stdout, stderr"
ms.date: "10/23/2018"
f1_keywords: ["CORECRT_WSTDIO/stdin", "CORECRT_WSTDIO/stderr", "CORECRT_WSTDIO/stdout", "stdin", "stderr", "stdout"]
helpviewer_keywords: ["stdout function", "standard output stream", "standard error stream", "stdin function", "standard input stream", "stderr function"]
ms.assetid: badd4735-596d-4498-857c-ec8b7e670e4c
---
# `stdin`, `stdout`, `stderr`

## Syntax

```C
FILE *stdin;
FILE *stdout;
FILE *stderr;
#include <stdio.h>
```

## Remarks

The **`stdin`**, **`stdout`**, and **`stderr`** global constant pointers are standard streams for input, output, and error output.

By default, standard input is read from the keyboard, while standard output and standard error are printed to the screen.

The following stream pointers are available to access the standard streams:

| Pointer | Stream |
|---|---|
| **`stdin`** | Standard input |
| **`stdout`** | Standard output |
| **`stderr`** | Standard error |

These pointers can be used as arguments to functions. Some functions, such as [`getchar`](./reference/getchar-getwchar.md) and [`putchar`](./reference/putchar-putwchar.md), use **`stdin`** and **`stdout`** automatically.

These pointers are constants, and can't be assigned new values. The [`freopen`](./reference/freopen-wfreopen.md) function can be used to redirect the streams to disk files or to other devices. The operating system allows you to redirect a program's standard input and output at the command level.

## See also

[Stream I/O](./stream-i-o.md)\
[Global constants](./global-constants.md)
