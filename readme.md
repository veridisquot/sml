# Small Maths Library

A lightweight, minimal and customisable maths library for C99,
generated by Lua.

## Generating
Requires Lua 5.3.

```
lua sml.lua
```

Generates a file named `sml.h`. Before including this file,
make sure to `#define SML_IMPL` in *one* C source file in
order to provide an implementation. Requires a C99-compatible
compiler.

The resulting header may be customised by changing the `config`
table at the top of `sml.lua`. Functions may be added by adding
to the `function_generator` table, in either the `global` sub-
table (run once), the `vector` sub-table (run for every vector)
or the `matrix` sub-table (run for every matrix).
