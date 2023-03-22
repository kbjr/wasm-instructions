
# `load` (load a value from memory and place it on the stack)

_todo_



| Opcode | Instruction    | Immediates                          | Stack Arity |
|--------|----------------|-------------------------------------|-------------|
| `0x28` | `i32.load`     | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i32 ]$ |
| `0x29` | `i64.load`     | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x2A` | `f32.load`     | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ f32 ]$ |
| `0x2B` | `f64.load`     | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ f64 ]$ |
| `0x2C` | `i32.load8_s`  | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i32 ]$ |
| `0x2D` | `i32.load8_u`  | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i32 ]$ |
| `0x2E` | `i32.load16_s` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i32 ]$ |
| `0x2F` | `i32.load16_u` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i32 ]$ |
| `0x30` | `i64.load8_s`  | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x31` | `i64.load8_u`  | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x32` | `i64.load16_s` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x33` | `i64.load16_u` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x34` | `i64.load32_s` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |
| `0x35` | `i64.load32_u` | $align_{u32},\enspace offset_{u32}$ | $[ i32 ] \to [ i64 ]$ |



## WAT Examples

### Loading a value from a constant address in memory

```wasm
;; Address to load from
i32.const 0

;; Load the value
i32.load
```



## References

[^§2.4.7]: _WebAssembly Core Specification: Memory Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#memory-instructions%E2%91%A0>

