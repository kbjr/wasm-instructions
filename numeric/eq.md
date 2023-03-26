
# eq (equals)

_todo_

$$
T.\mathsf{eq} \enspace ( a: T, b: T ) \to \begin{cases}
  1_{\mathsf{i32}} &\text{if } a = b\\
  0_{\mathsf{i32}} &\text{if } a \ne b
\end{cases}
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-----------|
| `0x46` | `i32.eq`    | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x51` | `i64.eq`    | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i32} ]$ |
| `0x5B` | `f32.eq`    | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{i32} ]$ |
| `0x61` | `f64.eq`    | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

_todo_


## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-ieq]: _Execution, Numerics, Integer Operations, ieq_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-ieq>
[^§4.3.3-feq]: _Execution, Numerics, Floating-Point Operations, feq_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-feq>

