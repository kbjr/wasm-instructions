
# `memory.grow` (request more memory)

Requests more memory be allocated to the WASM instance [^§2.4.7].

Takes one operand from the stack, an `i32` representing the number of pages to request [^§2.4.7]; Each page is defined as 64KiB [^§4.2.8].

Returns one result to the stack, an `i32` representing the previous total size of memory in pages, or `-1` if the operation failed [^§2.4.7].

$$
\mathsf{memory.grow} \enspace ( pages: \mathsf{i32} ) \to \mathsf{i32}
$$



## Instructions

| Opcode | Instruction   | Stack Arity |
|--------|---------------|-------------|
| `0x40` | `memory.grow` | $[ \mathsf{i32} ] \to [ \mathsf{i32} ]$ |



## WAT Examples

### Requesting more memory

```wasm
;; Places 2 on the stack
i32.const 2

;; Takes one value off of the stack (2), and requests
;; that many additional pages of memory
memory.grow

;; Places -1 on the stack
i32.const -1

;; Takes two values off of the stack (the result from
;; memory.grow and -1) and compares them
i32.eq

if
  ;; If the two values are equal, the instance failed
  ;; to get more memory
end
```



## References

### WebAssembly Core Specification

[^§2.4.7]: _Structure, Memory Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#memory-instructions>
[^§4.2.8]: _Execution, Runtime Structure, Memory Instances_ - <https://www.w3.org/TR/wasm-core-2/exec/runtime.html#memory-instances>
