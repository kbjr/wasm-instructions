
# add (addition)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6A` | `i32.add`   | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x7C` | `i64.add`   | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x92` | `f32.add`   | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{f32} ]$ |
| `0xA0` | `f64.add`   | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{f64} ]$ |



## WAT Examples

### Adding two constants

```wasm
;; Places 2 values on the stack
i32.const 10
i32.const 20

;; Takes two values off of the stack (10 and 20), adds them, and
;; places the result (30) on the stack
i32.add
```



## References

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.3.2.3]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, iaddn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-iaddmathrmiadd_n-i_1-i_2>
[^§4.3.3.3]: _WebAssembly Core Specification, Execution, Numerics, Floating-Point Operations, faddn_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-faddmathrmfadd_n-z_1-z_2>

