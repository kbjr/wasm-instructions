
# WASM Instructions

Download metadata for all instructions in either [JSON](./instructions?format=json) or [YAML](./instructions?format=yaml) formats.

## Numeric

- [`const`](./numeric/const)
- Comparisons
  - [`eqz`](./numeric/eqz) (equals zero)
  - [`eq`](./numeric/eq) (equals)
  - [`ne`](./numeric/ne) (not equals)
  - [`lt`](./numeric/lt) (less than)
  - [`gt`](./numeric/gt) (greater than)
  - [`le`](./numeric/le) (less than or equals)
  - [`ge`](./numeric/ge) (greater than or equals)


## Vector

_todo_

## Reference

_todo_

## Parametric

- [`drop`](./parametric/drop)
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
- `i32.store`
- `i64.store`
- `f32.store`
- `f64.store`
- `i32.store8`
- `i32.store16`
- `i64.store8`
- `i64.store16`
- `i64.store32`
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
