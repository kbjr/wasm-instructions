
# shuffle

Selects values from the vectors two in the two operands, combining them together to result in a new vector.

The lanes to select from are indicated using the immediates, with indices \[0-15] referring to the first operand, and \[16-31] referring to the second operand.

Any lane for which an out of bound index is provided will be set to 0 in the resulting vector.



| Opcode      | Instruction       | Immediates        | Stack Arity |
|-------------|-------------------|-------------------|-------------|
| `0xFD 0x0D` | `i8x16.shuffle`   | $const_{i32}[16]$ | $[ v128, v128 ] \to [ v128 ]$ |


## WAT Examples

```wasm
;; Create two vectors containing the values
v128.const i8x16 2 4 6 8 10 12 14 16 18 20 22 24 26 28 30 32
v128.const i8x16 1 3 5 7 9 11 13 15 17 19 21 23 25 27 29 31

;; The immediates define the ordered indices to select from the two vectors
i8x16.shuffle 0 31 1 30 2 29 3 28 4 27 5 26 6 25 7 24
;; The resulting vector looks like this:
;;  [ 2 31 4 29 6 27 8 25 10 23 12 21 14 19 16 17 ]
```


## References

[^§2.4.1]: _WebAssembly Core Specification: Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>

