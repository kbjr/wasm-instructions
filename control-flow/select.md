
# `select`

Selects one of the first two operands based on the value of the third operand [^§2.4.4].

The `valtype` immediate is optional, so long as the result type (and type of the first two operands) is a numeric type [^§2.4.4].

Otherwise, the `valtype` immediate declares the result type [^§2.4.4].



## Signatures

| Opcode | Signature |
|--------|-----------|
| `0x1B` | $select \quad [ numtype_1, numtype_1, i32 ] \to [ numtype_1 ]$ |
| `0x1C` | $select \quad valtype(T_1) \quad [ T_1, T_1, i32 ] \to [ T_1 ]$ |



## WAT Examples

### Without a `valtype` immediate

```wasm
;; The first operand will be the result if the condition is not 0
i32.const 10

;; The second operand will be the result if the condition is 0
i32.const 20

;; The third operand is the condition
i32.const 1
select
```


### With a `valtype` immediate

```wasm
;; The first operand will be the result if the condition is not 0
ref.func $func1

;; The second operand will be the result if the condition is 0
ref.func $func2

;; The third operand is the condition
i32.const 1
select funcref
```



## References

[^§2.4.4]: _WebAssembly Core Specification: Parametric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#parametric-instructions%E2%91%A0>

