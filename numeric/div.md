
# div (division)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6D` | `i32.div_s` | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x6E` | `i32.div_u` | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x7F` | `i64.div_s` | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x80` | `i64.div_u` | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x95` | `f32.div`   | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{f32} ]$ |
| `0xA3` | `f64.div`   | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{f64} ]$ |



## WAT Examples

### Dividing two constants

```wasm
;; Places 2 values on the stack
i32.const 20
i32.const 10

;; Takes two values off of the stack (20 and 10), divides, and
;; places the result (2) on the stack
i32.div_u
```



## References

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2.6]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, idiv_un_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-idiv-umathrmidiv_u_n-i_1-i_2>
[^§4.3.2.7]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, idiv_sn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-idiv-smathrmidiv_s_n-i_1-i_2>
[^§4.3.3.6]: _WebAssembly Core Specification, Execution, Numerics, Floating-Point Operations, fdivn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-fdivmathrmfdiv_n-z_1-z_2>

