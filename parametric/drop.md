
# `drop`

Drop one value from the stack [^§2.4.4] [^§4.4.4.1].



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x1A` | `drop`      | $[ T ] \to [ ]$ |



## WAT Examples

### Dropping a value from the stack

```wasm
;; Place something on the stack
i32.const 10

;; Drop the value off the stack
drop
```



## References

[^§2.4.4]: _WebAssembly Core Specification, Structure, Parametric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#parametric-instructions%E2%91%A0>
[^§4.4.4.1]: _WebAssembly Core Specification, Execution, Parametric Instructions, drop_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefsyntax-instr-parametricmathsfdrop%E2%91%A0>
