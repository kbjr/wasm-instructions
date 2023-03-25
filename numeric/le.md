
# le (less than or equals)

Takes 2 operands from the stack of the same numeric type and compares them.

Places an `i32` on the stack representing the result of the comparison: either 1 if the first operand is less than or equal to the second, or 0 otherwise [^§4.3.2-ile-u] [^§4.3.2-ile-s] [^§4.3.3-fle].

For integer types, there are two opcodes per type, to indicate whether to treat the operands as signed or unsigned for the comparison [^§2.4.1].

$$
T_\mathsf{numtype} \enspace
.\mathsf{le} \enspace \_s^? \enspace (a: T, b: T) \to \begin{cases}
  1_\mathsf{i32} &\text{if } a \le b \\
  0_\mathsf{i32} &\text{otherwise}
\end{cases}
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x4C` | `i32.le_s`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x4D` | `i32.le_u`  | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x5A` | `i64.le_s`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5B` | `i64.le_u`  | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5F` | `f32.le`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x65` | `f64.le`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ile-u]: _Execution, Numerics, Integer Operations, ile_u_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ile-u>
[^§4.3.2-ile-s]: _Execution, Numerics, Integer Operations, ile_s_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ile-s>
[^§4.3.3-fle]: _Execution, Numerics, Floating-Point Operations, fle_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fle>

