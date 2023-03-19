
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
i64.const 10

;; Places 20 on the stack
i64.const 20

;; Takes two values off of the stack (10 and 20), adds them, and
;; places the result (30) on the stack
i64.add
```


## References

[^§2.4.1]: _WebAssembly Core Specification: Numeric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#numeric-instructions%E2%91%A0>

