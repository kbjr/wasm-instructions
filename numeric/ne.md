
# ne (not equals)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x47` | `i32.ne`    | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x55` | `i64.ne`    | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5C` | `f32.ne`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x62` | `f64.ne`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ine]: _Execution, Numerics, Integer Operations, ine_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ine>
[^§4.3.3-fne]: _Execution, Numerics, Floating-Point Operations, fne_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fne>

