
# `memory.grow`

Requests more memory be allocated to the WASM instance [^§2.4.7].

Takes one parameter from the stack, an `i32` representing the number of pages to request [^§2.4.7]; Each page is defined as 64KiB [^§4.2.8].

Returns one result to the stack, an `i32` representing the previous total size of memory in pages, or `-1` if the operation failed [^§2.4.7].





## Signatures

| Opcode | Signature |
|--------|-----------|
| `0x40` | $memory.grow \quad [ i32 ] \to [ i32 ]$ |





## WAT Examples

### Requesting more memory

```wasm
i32.const 2    ;; Places 2 on the stack

memory.grow    ;; Takes one value off of the stack (2), and requests that
               ;; many additional pages of memory

i32.const -1   ;; Places -1 on the stack
i32.eq         ;; Takes two values off of the stack (-1 and the result from
               ;; memory.grow) and compares them

if
  ;; If the two values are equal, the instance failed to get more memory
end
```



## References

[^§2.4.7]: _WebAssembly Core Specification: Memory Instructions_ - <https://webassembly.github.io/spec/core/bikeshed/#memory-instructions%E2%91%A0>
[^§4.2.8]: _WebAssembly Core Specification: Memory Instances_ - <https://webassembly.github.io/spec/core/bikeshed/index.html#page-size>
