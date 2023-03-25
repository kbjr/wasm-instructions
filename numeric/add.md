
# add (addition)

Takes two operands (both of the same numeric type), adds them, and places the result on the stack [^§2.4.1] [^§4.3.2.3-iadd] [^§4.3.3.3-fadd].



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6A` | `i32.add`   | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x7C` | `i64.add`   | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x92` | `f32.add`   | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{f32} ]$ |
| `0xA0` | `f64.add`   | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{f64} ]$ |



!!! {.info}
### Example: Adding two constants

```wasm
;; Places 2 values on the stack
i32.const 10
i32.const 20

;; Takes two values off of the stack (10 and 20), adds them, and
;; places the result (30) on the stack
i32.add
```
!!!



## References

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2.3-iadd]: _Execution, Numerics, Integer Operations, iadd_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-iadd>
[^§4.3.3.3-fadd]: _Execution, Numerics, Floating-Point Operations, fadd_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fadd>
