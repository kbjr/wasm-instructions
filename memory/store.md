
# `store` (store an operand to memory)

_todo_



```katex:def
\def\u32{\text{u32}}
\def\i32{\text{i32}}
\def\i64{\text{i64}}
\def\f32{\text{f32}}
\def\f64{\text{f64}}
\def\memarg{\text{align}_\u32,\enspace\text{offset}_\u32}
```

| Opcode | Instruction    | Immediates | Stack Arity |
|--------|----------------|------------|-------------|
| `0x36` | `i32.store`    | $\memarg$  | $[ \i32, \i32 ] \to [ ]$ |
| `0x37` | `i64.store`    | $\memarg$  | $[ \i32, \i64 ] \to [ ]$ |
| `0x38` | `f32.store`    | $\memarg$  | $[ \i32, \f32 ] \to [ ]$ |
| `0x39` | `f64.store`    | $\memarg$  | $[ \i32, \f64 ] \to [ ]$ |
| `0x3A` | `i32.store8`   | $\memarg$  | $[ \i32, \i32 ] \to [ ]$ |
| `0x3B` | `i32.store16`  | $\memarg$  | $[ \i32, \i32 ] \to [ ]$ |
| `0x3C` | `i64.store8`   | $\memarg$  | $[ \i32, \i64 ] \to [ ]$ |
| `0x3D` | `i64.store16`  | $\memarg$  | $[ \i32, \i64 ] \to [ ]$ |
| `0x3E` | `i64.store32`  | $\memarg$  | $[ \i32, \i64 ] \to [ ]$ |



## WAT Examples

### Storing a value to a constant address in memory

```wasm
;; Address to store to
i32.const 0

;; The value to store
i32.const 10

;; Store the value
i32.store
```



## References

[^§2.4.7]: _WebAssembly Core Specification: Memory Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#memory-instructions%E2%91%A0>

