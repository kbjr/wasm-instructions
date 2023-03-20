
# shuffle (shuffle together lanes from two vectors using immediate indices)

Selects values from the two vector operands, combining them together to result in a new vector [^§4.4.3.7].

The lanes to select from are indicated using the immediates, with indices $[0-15]$ referring to the first operand, and $[16-31]$ referring to the second operand [^§4.4.3.7].



| Opcode    | Instruction       | Immediates       | Stack Arity |
|-----------|-------------------|------------------|-------------|
| `0xFD 13` | `i8x16.shuffle`   | $i5_{const}[16]$ | $[ v128, v128 ] \to [ v128 ]$ |


## WAT Examples

```wasm
;; Create two vectors containing the values
v128.const i8x16 1 3 5 7 9 11 13 15 17 19 21 23 25 27 29 31
v128.const i8x16 2 4 6 8 10 12 14 16 18 20 22 24 26 28 30 32

;; The immediates define the ordered indices to select from the two vectors
i8x16.shuffle 0 16 1 17 2 18 3 19 4 20 5 21 6 22 7 23
;; The resulting vector looks like this:
;;  [ 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 ]
```


## References

[^§2.4.2]: _WebAssembly Core Specification, Structure, Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>
[^§4.4.3.7]: _WebAssembly Core Specification, Execution, Vector Instructions, i8x16.shuffle_ - <https://webassembly.github.io/spec/core/bikeshed/#-mathsfi8x16hrefsyntax-instr-vecmathsfshufflexast>

