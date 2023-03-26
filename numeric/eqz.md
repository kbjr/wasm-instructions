
# eqz (equals zero)

_todo_

$$
T.\mathsf{eqz} \enspace ( value: T ) \to \begin{cases}
  1_{\mathsf{i32}} &\text{if } value = 0\\
  0_{\mathsf{i32}} &\text{otherwise}
\end{cases}
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x45` | `i32.eqz`   | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x50` | `i64.eqz`   | $[ \mathsf{i64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ieqz]: _Execution, Numerics, Integer Operations, ieqz_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ieqz>

