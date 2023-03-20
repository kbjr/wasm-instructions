
# add

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6A` | `i32.add`   | $[ i32, i32 ] \to [ i32 ]$ |
| `0x7C` | `i64.add`   | $[ i64, i64 ] \to [ i64 ]$ |
| `0x92` | `f32.add`   | $[ f32, f32 ] \to [ f32 ]$ |
| `0xA0` | `f64.add`   | $[ f64, f64 ] \to [ f64 ]$ |



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
<!-- [^§4.4.1.1]: _WebAssembly Core Specification, Execution, Numeric Instructions, t.const c_ - <https://webassembly.github.io/spec/core/bikeshed/#-tmathsfhrefsyntax-instr-numericmathsfconstc%E2%91%A0> -->

