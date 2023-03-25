
# sub (subtraction)

Takes two operands (both of the same numeric type), subtracts the second operand from the first, and places the result on the stack [^§2.4.1] [^§4.3.2-isub] [^§4.3.3-fsub].



| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6B` | `i32.sub`   | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x7D` | `i64.sub`   | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x93` | `f32.sub`   | $[ \mathsf{f32}, \mathsf{f32} ] \to [ \mathsf{f32} ]$ |
| `0xA1` | `f64.sub`   | $[ \mathsf{f64}, \mathsf{f64} ] \to [ \mathsf{f64} ]$ |



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

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-isub]: _Execution, Numerics, Integer Operations, isub_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-isub>
[^§4.3.3-fsub]: _Execution, Numerics, Floating-Point Operations, fsub_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-fsub>
