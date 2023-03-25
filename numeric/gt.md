
# gt (greater than)

Takes 2 operands from the stack of the same numeric type and compares them.

Places an `i32` on the stack representing the result of the comparison: either 1 if the first operand is greater than the second, or 0 otherwise [^§4.3.2-igt-u] [^§4.3.2-igt-s] [^§4.3.3-fgt].

For integer types, there are two opcodes per type, to indicate whether to treat the operands as signed or unsigned for the comparison [^§2.4.1].



## Signature

$$
\mathsf{gt} \enspace (a: \mathsf{numtype}_1, b: \mathsf{numtype}_1) \to \begin{cases}
  1_\mathsf{i32} &\text{if } a > b \\
  0_\mathsf{i32} &\text{otherwise}
\end{cases}
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x4A` | `i32.gt_s`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x4B` | `i32.gt_u`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x58` | `i64.gt_s`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x59` | `i64.gt_u`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5E` | `f32.gt`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x64` | `f64.gt`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-igt-u]: _Execution, Numerics, Integer Operations, igt_u_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-igt-u>
[^§4.3.2-igt-s]: _Execution, Numerics, Integer Operations, igt_s_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-igt-s>
[^§4.3.3-fgt]: _Execution, Numerics, Floating-Point Operations, fgt_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fgt>

