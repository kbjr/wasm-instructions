
# `memory.size`

_todo_



| Opcode | Instruction   | Stack Arity |
|--------|---------------|-------------|
| `0x3F` | `memory.size` | $[ ] \to [ \mathsf{i32} ]$ |



## WAT Examples

### Checking the current size of memory

```wasm
memory.size
```



## References

### WebAssembly Core Specification

[^§2.4.7]: _Structure, Memory Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#memory-instructions>
[^§4.2.8]: _Execution, Runtime Structure, Memory Instances_ - <https://www.w3.org/TR/wasm-core-2/exec/runtime.html#memory-instances>
