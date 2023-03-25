
# `memory.grow` (request more memory)

Requests more memory be allocated to the WASM instance [^§2.4.7].

Takes one operand from the stack, an `i32` representing the number of pages to request [^§2.4.7]; Each page is defined as 64KiB [^§4.2.8].

Returns one result to the stack, an `i32` representing the previous total size of memory in pages, or `-1` if the operation failed [^§2.4.7].



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

[^§2.4.7]: _WebAssembly Core Specification: Memory Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#memory-instructions%E2%91%A0>
[^§4.2.8]: _WebAssembly Core Specification: Memory Instances_ - <https://webassembly.github.io/spec/core/bikeshed/index.html#page-size>
