
# sub (subtraction)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6B` | `i32.sub`   | $[ \text{i32}, \text{i32} ] \to [ \text{i32} ]$ |
| `0x7D` | `i64.sub`   | $[ \text{i64}, \text{i64} ] \to [ \text{i64} ]$ |
| `0x93` | `f32.sub`   | $[ \text{f32}, \text{f32} ] \to [ \text{f32} ]$ |
| `0xA1` | `f64.sub`   | $[ \text{f64}, \text{f64} ] \to [ \text{f64} ]$ |



## WAT Examples

### Subtracting two constants

```wasm
;; Places 2 values on the stack
i32.const 20
i32.const 10

;; Takes two values off of the stack (20 and 10), subtracts, and
;; places the result (10) on the stack
i32.sub
```



## References

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.3.2.4]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, isubn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-isubmathrmisub_n-i_1-i_2>
[^§4.3.3.4]: _WebAssembly Core Specification, Execution, Numerics, Floating-Point Operations, fsubn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-fsubmathrmfsub_n-z_1-z_2>

