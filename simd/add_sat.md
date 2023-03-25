
# add_sat (saturating add)

_todo_



| Opcode     | Instruction       | Stack Arity |
|------------|-------------------|-------------|
| `0xFD 111` | `i8x16.add_sat_s` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 112` | `i8x16.add_sat_u` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 143` | `i16x8.add_sat_s` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 144` | `i16x8.add_sat_u` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |


## WAT Examples

_todo_


## References

[^§2.4.2]: _WebAssembly Core Specification, Structure, Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>
[^§4.3.2.42]: _WebAssembly Core Specification, Execution, Integer Operations, iaddsat_uN_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-iaddsat-umathrmiaddsat_u_n-i_1-i_2>
[^§4.3.2.43]: _WebAssembly Core Specification, Execution, Integer Operations, iaddsat_sN_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-iaddsat-smathrmiaddsat_s_n-i_1-i_2>
[^§4.3:sat]: _WebAssembly Core Specification, Execution, Numerics, Saturation of integers_ - <https://webassembly.github.io/spec/core/bikeshed/#aux-sat-u>
