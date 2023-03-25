
# rem (remainder)

_todo_



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6F` | `i32.rem_s` | $[ \text{i32}, \text{i32} ] \to [ \text{i32} ]$ |
| `0x70` | `i32.rem_u` | $[ \text{i32}, \text{i32} ] \to [ \text{i32} ]$ |
| `0x81` | `i64.rem_s` | $[ \text{i64}, \text{i64} ] \to [ \text{i64} ]$ |
| `0x82` | `i64.rem_u` | $[ \text{i64}, \text{i64} ] \to [ \text{i64} ]$ |



## WAT Examples

### Taking the remainder of dividing two constants

```wasm
;; Places 2 values on the stack
i32.const 23
i32.const 10

;; Takes two values off of the stack (23 and 10), divides, and
;; places the remainder (3) on the stack
i32.rem_u
```



## References

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.3.2.8]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, irem_un_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-irem-umathrmirem_u_n-i_1-i_2>
[^§4.3.2.9]: _WebAssembly Core Specification, Execution, Numerics, Integer Operations, $\text{irem_s}_{n}$_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-irem-smathrmirem_s_n-i_1-i_2>

