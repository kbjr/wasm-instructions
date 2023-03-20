
# const (declare vector constant)

Declares a vector constant value (of type `v128`), placing it on the stack [^§4.4.1.1]



| Opcode | Instruction | Immediates    | Stack Arity |
|--------|-------------|---------------|-------------|
| `0x41` | `i32.const` | $i32_{const}$ | $[ ] \to [ i32 ]$ |

!!! {.info}
For numeric values, see [`t.const`](../numeric/const.md)
!!!



## WAT Examples

### Adding two constants

```wasm
;; Places 10 on the stack
i32.const 10

;; Places 20 on the stack
i32.const 20

;; Takes two values off of the stack (10 and 20), adds them, and
;; places the result (30) on the stack
i64.add
```

### Different ways to declare integers

```wasm
i32.const 10
i32.const +20
i64.const -30

;; Integers can also be declared using hex format
i32.const 0x6D
```

### Different ways to declare floats

```wasm
f32.const 30.5
f32.const +32.57
f64.const -41.99

f64.const 12.34e+40

;; Hex-Float Format
f64.const 0x1p-1

;; Infinity
f64.const inf

;; NaN
f64.const nan
f64.const nan:0x123
```


## References

[^§2.4.1]: _WebAssembly Core Specification, Structure, Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>
[^§4.4.1.1]: _WebAssembly Core Specification, Execution, Numeric Instructions, t.const c_ - <https://webassembly.github.io/spec/core/bikeshed/#-tmathsfhrefsyntax-instr-numericmathsfconstc%E2%91%A0>

