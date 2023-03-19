
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
- Arithmetic
  - [`add`](./numeric/add)
  - [`sub`](./numeric/sub) (subtract)
  - [`mul`](./numeric/mul) (multiply)
  - [`div`](./numeric/div) (divide)
  - [`rem`](./numeric/rem) (remainder)
- Bit Operations
  - [`clz`](./numeric/clz) (count leading zeros)
  - [`ctz`](./numeric/ctz) (count trailing zeros)
  - [`popcnt`](./numeric/popcnt) (population count)
  - [`and`](./numeric/and) (bitwise and)
  - [`or`](./numeric/or) (bitwise or)
  - [`xor`](./numeric/xor) (bitwise xor)
  - [`shl`](./numeric/shl) (shift left)
  - [`shr`](./numeric/shr) (shift right)
  - [`rotl`](./numeric/rotl) (rotate left)
  - [`rotr`](./numeric/rotr) (rotate right)
- Float Operations
  - [`abs`](./numeric/abs) (absolute value)
  - [`neg`](./numeric/neg) (negative)
  - [`ceil`](./numeric/ceil) (ceiling / round up)
  - [`floor`](./numeric/floor) (floor / round down)
  - [`trunc`](./numeric/f.trunc)
  - [`nearest`](./numeric/nearest) (round to nearest)
  - [`sqrt`](./numeric/sqrt) (square root)
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


## Vector / SIMD

_todo_

## Reference

- [`ref.null`](./reference/null)
- [`ref.is_null`](./reference/is_null)
- [`ref.func`](./reference/func)

## Parametric

- [`drop`](./parametric/drop)
- [`select`](./parametric/select)

## Variable

- [`local.get`](./variable/local.get)
- [`local.set`](./variable/local.set)
- [`local.tee`](./variable/local.tee)
- [`global.get`](./variable/global.get)
- [`global.set`](./variable/global.set)

## Table

- [`table.get`](./table/table.get)
- [`table.set`](./table/table.set)
- _todo_

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
