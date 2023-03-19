
# add

_todo_



| Opcode      | Signature |
|-------------|-----------|
| `0xFD 0x6E` | $i8x16.add \quad [ v128, v128 ] \to [ v128 ]$ |
| `0xFD 0x6F` | $i8x16.add\_sat\_s \quad [ v128, v128 ] \to [ v128 ]$ |
| `0xFD 0x70` | $i8x16.add\_sat\_u \quad [ v128, v128 ] \to [ v128 ]$ |


| Opcode      | Instruction       | Stack Signature |
|-------------|-------------------|-----------------|
| `0xFD 0x6E` | `i8x16.add`       | $[ v128, v128 ] \to [ v128 ]$ |
| `0xFD 0x6F` | `i8x16.add_sat_s` | $[ v128, v128 ] \to [ v128 ]$ |
| `0xFD 0x70` | `i8x16.add_sat_u` | $[ v128, v128 ] \to [ v128 ]$ |


## WAT Examples

_todo_


## References

[^§2.4.1]: _WebAssembly Core Specification: Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>

