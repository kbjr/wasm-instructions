
# sub_sat (saturating subtract)

_todo_



| Opcode     | Instruction       | Stack Arity |
|------------|-------------------|-------------|
| `0xFD 114` | `i8x16.sub_sat_s` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 115` | `i8x16.sub_sat_u` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 146` | `i16x8.sub_sat_s` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |
| `0xFD 147` | `i16x8.sub_sat_u` | $[ \mathsf{v128}, \mathsf{v128} ] \to [ \mathsf{v128} ]$ |


## WAT Examples

_todo_

## References

[^§2.4.2]: _WebAssembly Core Specification, Structure, Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>
[^§4.3.2.44]: _WebAssembly Core Specification, Execution, Integer Operations, isubsat_uN_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-isubsat-umathrmisubsat_u_n-i_1-i_2>
[^§4.3.2.45]: _WebAssembly Core Specification, Execution, Integer Operations, isubsat_sN_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefop-isubsat-smathrmisubsat_s_n-i_1-i_2>
[^§4.3:sat]: _WebAssembly Core Specification, Execution, Numerics, Saturation of integers_ - <https://webassembly.github.io/spec/core/bikeshed/#aux-sat-u>
