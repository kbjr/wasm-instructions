
# rem (remainder)

_todo_

$$
T.\mathsf{rem}\_s \enspace ( a: T, b: T ) \to a\mod b
$$



## Instructions

| Opcode | Instruction | Stack Arity |
|--------|-------------|-------------|
| `0x6F` | `i32.rem_s` | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x70` | `i32.rem_u` | $[ \mathsf{i32}, \mathsf{i32} ] \to [ \mathsf{i32} ]$ |
| `0x81` | `i64.rem_s` | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |
| `0x82` | `i64.rem_u` | $[ \mathsf{i64}, \mathsf{i64} ] \to [ \mathsf{i64} ]$ |



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

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.3.2-irem-u]: _Execution, Numerics, Integer Operations, irem_u_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-irem-u>
[^§4.3.2-irem-s]: _Execution, Numerics, Integer Operations, irem_s_ - <https://www.w3.org/TR/wasm-core-2/exec/numerics.html#op-irem-s>

