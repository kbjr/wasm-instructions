
# const (declare vector constant)

Declares a vector constant value (of type `v128`), placing it on the stack [^§4.4.1.1]



| Opcode    | Instruction  | Immediates     | Stack Arity |
|-----------|--------------|----------------|-------------|
| `0xFD 12` | `v128.const` | $\text{v128}_\text{const}$ | $[ ] \to [ \text{v128} ]$ |

!!! {.info}
For numeric values, see [`t.const`](../numeric/const.md)
!!!



## WAT Examples

### Defining different shapes of vectors

```wasm
v128.const i8x16 2 4 6 8 10 12 14 16 18 20 22 24 26 28 30 32

v128.const i16x8 2 4 6 8 10 12 14 16

v128.const i32x4 2 4 6 8

v128.const i64x2 2 4

v128.const f32x4 2.1 4.2 6.3 8.4

v128.const f64x2 2.1 4.2
```


## References

[^§2.4.2]: _WebAssembly Core Specification, Structure, Vector Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#vector-instructions%E2%91%A0>
[^§4.4.3.1]: _WebAssembly Core Specification, Execution, Vector Instructions, v128.const c_ - <https://webassembly.github.io/spec/core/bikeshed/#-hrefsyntax-valtypemathsfv128mathsfhrefsyntax-instr-vecmathsfconstc%E2%91%A0>

