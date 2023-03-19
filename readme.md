
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
- Bitwise
  - [`clz`](./numeric/clz)
  - [`ctz`](./numeric/ctz)
  - [`popcnt`](./numeric/popcnt)
  - [`and`](./numeric/and)
  - [`or`](./numeric/or)
  - [`xor`](./numeric/xor)
  - [`shl`](./numeric/shl)
  - [`shr`](./numeric/shr)
  - [`rotl`](./numeric/rotl)
  - [`rotr`](./numeric/rotr)
- Arithmetic
  - [`add`](./numeric/add)
  - [`sub`](./numeric/sub)
  - [`mul`](./numeric/mul)
  - [`div`](./numeric/div)
  - [`rem`](./numeric/rem)
- Float Operations
  - [`abs`](./numeric/abs)
  - [`neg`](./numeric/neg)
  - [`ceil`](./numeric/ceil)
  - [`floor`](./numeric/floor)
  - [`trunc`](./numeric/f.trunc)
  - [`nearest`](./numeric/nearest)
  - [`sqrt`](./numeric/sqrt)
  - [`min`](./numeric/min)
  - [`max`](./numeric/max)
  - [`copysign`](./numeric/copysign)
- Type Convertion
  - [`wrap`](./numeric/wrap)
  - [`trunc`](./numeric/i.trunc)
  - [`trunc_sat`](./numeric/trunc_sat)
  - [`extend`](./numeric/extend)
  - [`convert`](./numeric/convert)
  - [`demote`](./numeric/demote)
  - [`promote`](./numeric/promote)
  - [`reinterpret`](./numeric/reinterpret)


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
