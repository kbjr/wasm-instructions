
# splat (create vector with identical lanes)

Creates a new vector by repeating the given operand value for each lane and places the new vector on the stack [^§4.4.3.8]

There are 6 opcodes, to indicate the size of the operand and shape of the resulting vector



| Opcode    | Instruction   | Stack Arity |
|-----------|---------------|-------------|
| `0xFD 15` | `i8x16.splat` | $[ i32 ] \to [ v128 ]$ |
| `0xFD 16` | `i16x8.splat` | $[ i32 ] \to [ v128 ]$ |
| `0xFD 17` | `i32x4.splat` | $[ i32 ] \to [ v128 ]$ |
| `0xFD 18` | `i64x2.splat` | $[ i64 ] \to [ v128 ]$ |
| `0xFD 19` | `f32x4.splat` | $[ f32 ] \to [ v128 ]$ |
| `0xFD 20` | `f64x2.splat` | $[ f64 ] \to [ v128 ]$ |




## WAT Examples

### Creating a vector be repeating a constant

```wasm
;; Place a value (10) on the stack to be the repeated operand
i32.const 10

i8x16.splat
;; Resulting vector contains the operand value (10) repeated in
;; each lane, i.e.
;;  [ 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10 ]
```


## References

[^§2.4.2]: _WebAssembly Core Specification, Structure, Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>
[^§4.4.3.8]: _WebAssembly Core Specification, Execution, Vector Instructions, shape.splat_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefsyntax-shapemathitshapemathsfhrefsyntax-instr-vecmathsfsplat%E2%91%A0>

