
# `select`

Selects one of the first two parameters based on the value of the third parameter [^§2.4.4].




## Signatures

| Opcode | Signature |
|--------|-----------|
| `0x1B` | $select \quad [ numtype_1, numtype_1, i32 ] \to [ numtype_1 ]$ |
| `0x1C` | $select \quad valtype(T_1) \quad [ T_1, T_1, i32 ] \to [ T_1 ]$ |







## WAT Examples

### Without a `valtype` immediate

```wasm
i32.const 10    ;; The first parameter will be the result if
                ;; the condition is not 0
                
i32.const 20    ;; The second parameter will be the result if
                ;; the condition is 0

i32.const 1     ;; The third parameter is the condition
select
```

### With a `valtype` immediate

```wasm
i32.const 10    ;; The first parameter will be the result if
                ;; the condition is not 0

i32.const 20    ;; The second parameter will be the result if
                ;; the condition is 0

i32.const 1     ;; The third parameter is the condition
select i32
```




## References

[^§2.4.4]: _WebAssembly Core Specification: Parametric Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#parametric-instructions%E2%91%A0>

