
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
i32.const 10    ;; "true" result
i32.const 20    ;; "false" result

i32.const 1     ;; condition
select
```

### With a `valtype` immediate

```wasm
i32.const 10    ;; "true" result
i32.const 20    ;; "false" result

i32.const 1     ;; condition
select i32
```




## References

[^§2.3.4]: https://webassembly.github.io/spec/core/bikeshed/index.html#syntax-valtype
[^§2.4.4]: https://webassembly.github.io/spec/core/bikeshed/#parametric-instructions%E2%91%A0

