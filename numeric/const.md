
# Numeric Constants

Declares a numeric constant value (of type `i32`, `i64`, `f32`, or `f64`), placing it on the stack [^§2.4.1]

There are four different opcodes, to indicate the type of the value




## Signatures

| Opcode | Signature |
|--------|-----------|
| `0x41` | $i32.const \quad const_{i32} \quad [ ] \to [ i32 ]$ |
| `0x42` | $i64.const \quad const_{i64} \quad [ ] \to [ i64 ]$ |
| `0x43` | $f32.const \quad const_{f32} \quad [ ] \to [ f32 ]$ |
| `0x44` | $f64.const \quad const_{f64} \quad [ ] \to [ f64 ]$ |



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

### Declaring constants different types of constants in different ways

```wasm
;; Integers
i32.const 10
i32.const +20
i64.const -30

;; Integers can also be declared using hex format
i32.const 0x6D


;; Floats
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

[^§2.4.1]: _WebAssembly Core Specification: Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>

