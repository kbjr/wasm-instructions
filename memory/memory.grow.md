
# `memory.grow`

Requests more memory be allocated to the WASM instance.

Takes one parameter from the stack, an `i32` representing the number of pages to request; Each page is defined as 64KiB.

Returns one result to the stack, an `i32` representing the previous total size of memory in pages, or `-1` if the operation failed.

```
memory.grow ( i32 ) => ( i32 )
```

```katex
memory.grow [ i32 ] \to [ i32 ]
```

|  |  |
|--|--|
| Opcode | `0x40` |
| Immediates | _none_ |
| Parameters | `i32` |
| Results | `i32` |



## Examples

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
