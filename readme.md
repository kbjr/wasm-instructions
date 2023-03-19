
# WASM Instructions

Download metadata for all instructions in either [JSON](./instructions?format=json) or [YAML](./instructions?format=yaml) formats.

## Numeric

- [`const`](./numeric/const)
- Comparisons
  - [`eqz`](./numeric/eqz)
  - [`eq`](./numeric/eq)
  - [`ne`](./numeric/ne)
  - [`lt`](./numeric/lt)
  - [`gt`](./numeric/gt)
  - [`le`](./numeric/le)
  - [`ge`](./numeric/ge)

- `i32.eqz`
- `i32.eq`
- `i32.ne`
- `i32.lt_s`
- `i32.lt_u`
- `i32.gt_s`
- `i32.gt_u`
- `i32.le_s`
- `i32.le_u`
- `i32.ge_s`
- `i32.ge_u`
- `i64.eqz`
- `i64.eq`
- `i64.ne`
- `i64.lt_s`
- `i64.lt_u`
- `i64.gt_s`
- `i64.gt_u`
- `i64.le_s`
- `i64.le_u`
- `i64.ge_s`
- `i64.ge_u`
- `f32.eq`
- `f32.ne`
- `f32.lt`
- `f32.gt`
- `f32.le`
- `f32.ge`
- `f64.eq`
- `f64.ne`
- `f64.lt`
- `f64.gt`
- `f64.le`
- `f64.ge`

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
