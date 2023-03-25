
# `store` (store an operand to memory)

_todo_



| Opcode | Instruction    | Immediates    | Stack Arity |
|--------|----------------|---------------|-------------|
| `0x36` | `i32.store`    | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i32} ] \to [ ]$ |
| `0x37` | `i64.store`    | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i64} ] \to [ ]$ |
| `0x38` | `f32.store`    | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{f32} ] \to [ ]$ |
| `0x39` | `f64.store`    | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{f64} ] \to [ ]$ |
| `0x3A` | `i32.store8`   | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i32} ] \to [ ]$ |
| `0x3B` | `i32.store16`  | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i32} ] \to [ ]$ |
| `0x3C` | `i64.store8`   | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i64} ] \to [ ]$ |
| `0x3D` | `i64.store16`  | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i64} ] \to [ ]$ |
| `0x3E` | `i64.store32`  | $\mathsf{align}_\mathsf{i32},\enspace\mathsf{offset}_\mathsf{i32}$ | $[ \mathsf{i32}, \mathsf{i64} ] \to [ ]$ |



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

[^§2.4.7]: _WebAssembly Core Specification, Structure, Memory Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.4.7.6]: _WebAssembly Core Specification, Execution, Memory Instructions, t.store memarg and t.storeN memarg_ - <https://webassembly.github.io/spec/core/bikeshed/#-tmathsfhrefsyntax-instr-memorymathsfstorehrefsyntax-memargmathitmemarg-and--tmathsfhrefsyntax-instr-memorymathsfstorenhrefsyntax-memargmathitmemarg>

