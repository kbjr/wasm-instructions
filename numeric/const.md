
# const (declare constant)

Declares a numeric constant value (of type `i32`, `i64`, `f32`, or `f64`), placing it on the stack [^§4.4.1.1]

There are four different opcodes, to indicate the type of the value [^§2.4.1]



| Opcode | Instruction | Immediates    | Stack Arity |
|--------|-------------|---------------|-------------|
| `0x41` | `i32.const` | $i32_{const}$ | $[ ] \to [ i32 ]$ |
| `0x42` | `i64.const` | $i64_{const}$ | $[ ] \to [ i64 ]$ |
| `0x43` | `f32.const` | $f32_{const}$ | $[ ] \to [ f32 ]$ |
| `0x44` | `f64.const` | $f64_{const}$ | $[ ] \to [ f64 ]$ |

!!! {.info}
For SIMD / Vectors, see [`v128.const`](../simd/const.md)
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
i32.add
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

