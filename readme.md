
# WASM Instructions

Download metadata for all instructions in either [JSON](./instructions?format=json) or [YAML](./instructions?format=yaml) formats.

## Numeric

### Constants

- [`i32.const`](./numeric/i32.const)
- [`i64.const`](./numeric/i64.const)
- [`f32.const`](./numeric/f32.const)
- [`f64.const`](./numeric/f64.const)

## Vector

_todo_

## Reference

_todo_

## Parametric

- `drop`
- [`select`](./parametric/select)

## Variable

- `local.get`
- `local.set`
- `local.tee`
- `global.get`
- `global.set`

## Table

- `table.get`
- `table.set`
_todo_

## Memory

- `i32.load`
- `i64.load`
- `f32.load`
- `f64.load`
- `i32.load8_s`
- `i32.load8_u`
- `i32.load16_s`
- `i32.load16_u`
- `i64.load8_s`
- `i64.load8_u`
- `i64.load16_s`
- `i64.load16_u`
- `i64.load32_s`
- `i64.load32_u`
- `memory.size`
- [`memory.grow`](./memory/memory.grow)

## Control

- `unreachable`
- `nop`
- `block`
- `loop`
- `if`
- `else`
- `end`
- `br`
- `br_if`
- `br_table`
- `return`
- `call`
- `call_indirect`
