
# swizzle

Selects values from the first vector operand to form a new vector [^§4.4.3.6].

The lanes to select from are indicated using the second vector operand, with indices $[0-15]$ referring to the first operand [^§4.4.3.6].

Any lane for which an out of bound index is provided will be set to 0 in the resulting vector [^§4.4.3.6].



| Opcode    | Instruction       | Stack Arity |
|-----------|-------------------|-------------|
| `0xFD 13` | `i8x16.swizzle`   | $[ v128, v128 ] \to [ v128 ]$ |


## WAT Examples

```wasm
;; Create a vector containing the values
v128.const i8x16 2 4 6 8 10 12 14 16 18 20 22 24 26 28 30 32

;; Create a vector representing the ordered indices to select
v128.const i8x16 9 2 3 1 6 4 7 8 15 12 0 5 10 11 13 14

i8x16.swizzle
;; The resulting vector looks like:
;;  [ 20 6 8 4 14 10 16 18 32 26 2 12 22 24 28 30 ]
```


## References

[^§4.4.3.6]: _WebAssembly Core Specification, Execution, Vector Instructions, i8x16.swizzle_ - <https://webassembly.github.io/spec/core/bikeshed/#-mathsfi8x16hrefsyntax-instr-vecmathsfswizzle%E2%91%A0>

