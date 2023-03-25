
# lt (less than)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x48` | `i32.lt_s`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x49` | `i32.lt_u`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x56` | `i64.lt_s`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x57` | `i64.lt_u`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5D` | `f32.lt`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x63` | `f64.lt`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ilt-u]: _Execution, Numerics, Integer Operations, ilt_u_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ilt-u>
[^§4.3.2-ilt-s]: _Execution, Numerics, Integer Operations, ilt_s_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ilt-s>
[^§4.3.3-flt]: _Execution, Numerics, Floating-Point Operations, flt_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-flt>

