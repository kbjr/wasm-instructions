
# mul (multiplication)

_todo_

$$
T.\mathsf{mul} \enspace ( a: T, b: T ) \to (a \times b)_T
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6C` | `i32.mul`   | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x7E` | `i64.mul`   | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x94` | `f32.mul`   | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{f32} ]$ |
| `0xA2` | `f64.mul`   | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{f64} ]$ |



## WAT Examples

### Mulitiplying two constants

```wasm
;; Places 2 values on the stack
i32.const 20
i32.const 10

;; Takes two values off of the stack (20 and 10), multiplies, and
;; places the result (200) on the stack
i32.mul
```



## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-imul]: _Execution, Numerics, Integer Operations, imul_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-imul>
[^§4.3.3-fmul]: _Execution, Numerics, Floating-Point Operations, fmul_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fmul>
