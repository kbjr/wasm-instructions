
# const (declare constant)

Declares a numeric constant value (of type `i32`, `i64`, `f32`, or `f64`), placing it on the stack [^§4.4.1-const]

There are four different opcodes, to indicate the type of the value [^§2.4.1]

$$
T_\mathsf{numtype} \enspace
.\mathsf{const} \enspace
T_\mathsf{const} \enspace ( \enspace ) \to T
$$



## Instructions

| Opcode | Instruction | Immediates    | Stack Arity |
|--------|-------------|---------------|-------------|
| `0x41` | `i32.const` | $\mathsf{i32}_\mathsf{const}$ | $[ ] \to [ \mathsf{i32} ]$ |
| `0x42` | `i64.const` | $\mathsf{i64}_\mathsf{const}$ | $[ ] \to [ \mathsf{i64} ]$ |
| `0x43` | `f32.const` | $\mathsf{f32}_\mathsf{const}$ | $[ ] \to [ \mathsf{f32} ]$ |
| `0x44` | `f64.const` | $\mathsf{f64}_\mathsf{const}$ | $[ ] \to [ \mathsf{f64} ]$ |

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

### WebAssembly Core Specification

[^§2.4.1]: _Structure, Numeric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#numeric-instructions>
[^§4.4.1-const]: _Execution, Numeric Instructions, const_ - <https://www.w3.org/TR/wasm-core-2/exec/instructions.html#exec-const>

