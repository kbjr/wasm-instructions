
# `load` (load a value from memory and place it on the stack)

Loads a value from memory and places it on the stack.

For integer types, there are additional opcodes to allow loading values smaller than result data type (e.g. placing an `i32` on the stack, but only loading 8 bits from memory); These also come in two forms each, to indicate whether the value read from memory should be interpretted as signed or unsigned.

$$
T_\mathsf{numtype}
\enspace .\mathsf{load}
\enspace N\_s^?
% \enspace \mathsf{memarg}
\enspace \mathsf{offset}_\mathsf{i32}
\enspace \mathsf{align}_\mathsf{i32}
\enspace (ptr: \mathsf{i32}) \to T
$$

## Instructions

| Opcode | Instruction    | Immediates    | Stack Arity |
|--------|----------------|---------------|-------------|
| `0x28` | `i32.load`     | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x29` | `i64.load`     | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x2A` | `f32.load`     | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{f32} ]$ |
| `0x2B` | `f64.load`     | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{f64} ]$ |
| `0x2C` | `i32.load8_s`  | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x2D` | `i32.load8_u`  | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x2E` | `i32.load16_s` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x2F` | `i32.load16_u` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x30` | `i64.load8_s`  | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x31` | `i64.load8_u`  | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x32` | `i64.load16_s` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x33` | `i64.load16_u` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x34` | `i64.load32_s` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |
| `0x35` | `i64.load32_u` | $\mathsf{offset}_\mathsf{i32}, \enspace \mathsf{align}_\mathsf{i32}$ | $[ \mathsf{i32} ] \to [ \mathsf{i64} ]$ |



## WAT Examples

### Loading a value from a constant address in memory

```wasm
;; Address to load from
i32.const 0

;; Load the value
i32.load
```



## References

### WebAssembly Core Specification

[^§2.4.7]: _Structure, Memory Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#memory-instructions>
[^§4.4.7-load]: _Execution, Memory Instructions, load_ - <https://www.w3.org/TR/wasm-core-2/exec/instructions.html#exec-load>
