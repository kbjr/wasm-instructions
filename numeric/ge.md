
# ge (greater than or equals)

Takes 2 operands from the stack of the same numeric type and compares them.

Places an `i32` on the stack representing the result of the comparison: either 1 if the first operand is greater than or equal to the second, or 0 otherwise [^§4.3.2-ige-u] [^§4.3.2-ige-s] [^§4.3.3-fge].

For integer types, there are two opcodes per type, to indicate whether to treat the operands as signed or unsigned for the comparison [^§2.4.1].

$$
T.\mathsf{ge}\_s^? \enspace (a: T, b: T) \to \begin{cases}
  1_\mathsf{i32} &\text{if } a \ge b \\
  0_\mathsf{i32} &\text{otherwise}
\end{cases}
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x4E` | `i32.ge_s`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x4F` | `i32.ge_u`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x5C` | `i64.ge_s`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5D` | `i64.ge_u`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x60` | `f32.ge`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x66` | `f64.ge`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ige-u]: _Execution, Numerics, Integer Operations, ige_u_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ige-u>
[^§4.3.2-ige-s]: _Execution, Numerics, Integer Operations, ige_s_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ige-s>
[^§4.3.3-fge]: _Execution, Numerics, Floating-Point Operations, fge_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fge>

