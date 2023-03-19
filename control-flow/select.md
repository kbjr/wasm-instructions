
# `select`

_todo: description_




## Signatures

| Opcode | Signature |
|--------|-----------|
| `0x1B` | $select \quad [ numtype_1, numtype_1, i32 ] \to [ numtype_1 ]$ |
| `0x1C` | $select \quad valtype(T_1) \quad [ T_1, T_1, i32 ] \to [ T_1 ]$ |







## Examples

```wasm
i32.const 10    ;; "true" result
i32.const 20    ;; "false" result

i32.const 1     ;; condition
select
```
