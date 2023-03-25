
# `drop`

Drop one value from the stack [^§2.4.4] [^§4.4.4-drop].

$$
\mathsf{drop} \enspace (T) \to \varnothing
$$



## Instructions

| Opcode | Instruction | Stack Arity     |
|--------|-------------|-----------------|
| `0x1A` | `drop`      | $[ T ] \to [ ]$ |



## WAT Examples

### Dropping a value from the stack

```wasm
;; Place something on the stack
i32.const 10

;; Drop the value off the stack
drop
```



## References

### WebAssembly Core Specification

[^§2.4.4]: _Structure, Parametric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#parametric-instructions>
[^§4.4.4-drop]: _Execution, Parametric Instructions, drop_ - <https://www.w3.org/TR/wasm-core-2/exec/instructions.html#exec-drop>
