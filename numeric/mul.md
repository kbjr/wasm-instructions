
# mul (multiplication)

_todo_



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

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.3.2.5]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, imuln_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-imulmathrmimul_n-i_1-i_2>
[^§4.3.3.5]: _WebAssembly Core Specification, Execution, Numerics, Floating-Point Operations, fmuln_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-fmulmathrmfmul_n-z_1-z_2>

