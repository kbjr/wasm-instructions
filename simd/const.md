
# const (declare vector constant)

Declares a vector constant value (of type `v128`), placing it on the stack [^§4.4.1.1]

$$
\mathsf{v128.const} \enspace
S_\mathsf{shape} \enspace
const(\mathsf{v128}, S)
\enspace
( \enspace ) \to \mathsf{v128}

\\
\mathstrut
\\

const(\mathsf{v128}, S_{\mathsf{shape}}) = 
\begin{cases}
  [ const(\mathsf{i8})_1, const(\mathsf{i8})_2, ..., const(\mathsf{i8})_{16} ]
    &\text{if } S = \text{i8x16} \\
  [ const(\mathsf{i16})_1, const(\mathsf{i16})_2, ..., const(\mathsf{i16})_8 ]
    &\text{if } S = \text{i16x8} \\
  [ const(\mathsf{i32})_1, const(\mathsf{i32})_2, const(\mathsf{i32})_3, const(\mathsf{i32})_4 ]
    &\text{if } S = \text{i32x4} \\
  [ const(\mathsf{i64})_1, const(\mathsf{i64})_2 ]
    &\text{if } S = \text{i64x2} \\
  [ const(\mathsf{f32})_1, const(\mathsf{f32})_2, const(\mathsf{f32})_3, const(\mathsf{f32})_4 ]
    &\text{if } S = \text{f32x4} \\
  [ const(\mathsf{f64})_1, const(\mathsf{f64})_2 ]
    &\text{if } S = \text{f64x2} \\
\end{cases}
$$



## Instructions

| Opcode    | Instruction  | Immediates     | Stack Arity |
|-----------|--------------|----------------|-------------|
| `0xFD 12` | `v128.const` | $const(\mathsf{v128})$ | $[ ] \to [ \mathsf{v128} ]$ |

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

