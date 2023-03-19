
# `select`

_todo: description_




## Signature

```katex
T_1 ::= numtype
\newline
select \quad [ T_1, T_1, i32 ] \to [ T_1 ]
```

```katex
T_1 ::= valtype
\newline
select \quad valtype(T_1) \quad [ T_1, T_1, i32 ] \to [ T_1 ]
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
