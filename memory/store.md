
# `store` (store an operand to memory)

_todo_



| Opcode | Instruction    | Immediates | Stack Arity |
|--------|----------------|------------|-------------|
| `0x36` | $\text{i32.store}$    | $\wasmmemarg$  | $[ \text{i32}, \text{i32} ] \to [ ]$ |
| `0x37` | $\text{i64.store}$    | $\wasmmemarg$  | $[ \text{i32}, \text{i64} ] \to [ ]$ |
| `0x38` | $\text{f32.store}$    | $\wasmmemarg$  | $[ \text{i32}, \text{f32} ] \to [ ]$ |
| `0x39` | $\text{f64.store}$    | $\wasmmemarg$  | $[ \text{i32}, \text{f64} ] \to [ ]$ |
| `0x3A` | $\text{i32.store8}$   | $\wasmmemarg$  | $[ \text{i32}, \text{i32} ] \to [ ]$ |
| `0x3B` | $\text{i32.store16}$  | $\wasmmemarg$  | $[ \text{i32}, \text{i32} ] \to [ ]$ |
| `0x3C` | $\text{i64.store8}$   | $\wasmmemarg$  | $[ \text{i32}, \text{i64} ] \to [ ]$ |
| `0x3D` | $\text{i64.store16}$  | $\wasmmemarg$  | $[ \text{i32}, \text{i64} ] \to [ ]$ |
| `0x3E` | $\text{i64.store32}$  | $\wasmmemarg$  | $[ \text{i32}, \text{i64} ] \to [ ]$ |



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

