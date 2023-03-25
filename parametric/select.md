
# `select`

Selects one of the first two operands based on the value of the third operand [^§2.4.4] [^§4.4.4-select].

The `valtype` immediate is optional, so long as the result type (and type of the first two operands) is a numeric type [^§2.4.4].

Otherwise, the `valtype` immediate declares the result type [^§2.4.4].



| Opcode | Instruction | Immediates              | Stack Arity |
|--------|-------------|-------------------------|-------------|
| `0x1B` | `select`    | _none_                  | $[ \mathsf{numtype}_1, \mathsf{numtype}_1, \mathsf{i32} ] \to [ \mathsf{numtype}_1 ]$ |
| `0x1C` | `select`    | $\mathsf{valtype}(T_1)$ | $[ T_1, T_1, \mathsf{i32} ] \to [ T_1 ]$ |



## WAT Examples

### Without a `valtype` immediate

```wasm
;; The first operand will be the result if the condition is not 0
i32.const 10

;; The second operand will be the result if the condition is 0
i32.const 20

;; The third operand is the condition
i32.const 1
select
```


### With a `valtype` immediate

```wasm
;; The first operand will be the result if the condition is not 0
ref.func $func1

;; The second operand will be the result if the condition is 0
ref.func $func2

;; The third operand is the condition
i32.const 1
select funcref
```



## References

### WebAssembly Core Specification

[^§2.4.4]: _Structure, Parametric Instructions_ - <https://www.w3.org/TR/wasm-core-2/syntax/instructions.html#parametric-instructions>
[^§4.4.4-select]: _Execution, Parametric Instructions, select(t*)_ - <https://www.w3.org/TR/wasm-core-2/exec/instructions.html#exec-select>

