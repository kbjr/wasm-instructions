
# WASM Instructions

Download metadata for all instructions in either [JSON](./instructions?format=json) or [YAML](./instructions?format=yaml) formats.

## Numeric

These instructions pertain to the 4 "main" numeric data types: `i32`, `i64`, `f32`, and `f64`

- [`const`](./numeric/const.md) (declare constant)
- Comparisons
  - [`eqz`](./numeric/eqz.md) (equals zero)
  - [`eq`](./numeric/eq.md) (equals)
  - [`ne`](./numeric/ne.md) (not equals)
  - [`lt`](./numeric/lt.md) (less than)
  - [`gt`](./numeric/gt.md) (greater than)
  - [`le`](./numeric/le.md) (less than or equals)
  - [`ge`](./numeric/ge.md) (greater than or equals)
- Arithmetic
  - [`add`](./numeric/add.md)
  - [`sub`](./numeric/sub.md) (subtract)
  - [`mul`](./numeric/mul.md) (multiply)
  - [`div`](./numeric/div.md) (divide)
  - [`rem`](./numeric/rem.md) (remainder)
- Bitwise Operations
  - [`clz`](./numeric/clz.md) (count leading zeros)
  - [`ctz`](./numeric/ctz.md) (count trailing zeros)
  - [`popcnt`](./numeric/popcnt.md) (population count)
  - [`and`](./numeric/and.md) (bitwise and)
  - [`or`](./numeric/or.md) (bitwise or)
  - [`xor`](./numeric/xor.md) (bitwise xor)
  - [`shl`](./numeric/shl.md) (shift left)
  - [`shr`](./numeric/shr.md) (shift right)
  - [`rotl`](./numeric/rotl.md) (rotate left)
  - [`rotr`](./numeric/rotr.md) (rotate right)
- Floating Point Operations
  - [`abs`](./numeric/abs.md) (absolute value)
  - [`neg`](./numeric/neg.md) (negative)
  - [`ceil`](./numeric/ceil.md) (ceiling / round up)
  - [`floor`](./numeric/floor.md) (floor / round down)
  - [`trunc`](./numeric/f.trunc.md) (truncate)
  - [`nearest`](./numeric/nearest.md) (round to nearest)
  - [`sqrt`](./numeric/sqrt.md) (square root)
  - [`min`](./numeric/min.md) (select minimum)
  - [`max`](./numeric/max.md) (select maximum)
  - [`copysign`](./numeric/copysign.md)
- Type Convertion
  - [`wrap`](./numeric/wrap.md)
  - [`trunc`](./numeric/i.trunc.md)
  - [`trunc_sat`](./numeric/trunc_sat.md)
  - [`extend`](./numeric/extend.md)
  - [`convert`](./numeric/convert.md)
  - [`demote`](./numeric/demote.md)
  - [`promote`](./numeric/promote.md)
  - [`reinterpret`](./numeric/reinterpret.md)


## Vector / SIMD

These instructions pertain to `v128` values, and their various formats.

<!-- https://github.com/WebAssembly/simd/blob/main/proposals/simd/SIMD.md -->

- [`const`](./simd/const.md) (declare constant vector)
- [`splat`](./simd/splat.md) (create vector with identical lanes)
- Memory
  - [`load`](./simd/load.md)
  - [`store`](./simd/store.md)
- Lane Operations
  - [`shuffle`](./simd/shuffle.md) (shuffle together lanes from two vectors using immediate indices)
  - [`swizzle`](./simd/swizzle.md) (swizzle lanes using stack indices)
  - `extract_lane` (get lane value)
  - `replace_lane` (set lane value)
- `narrow`
- Comparisons
  - [`eq`](./simd/eq.md) (equals)
  - [`ne`](./simd/ne.md) (not equals)
  - [`lt`](./simd/lt.md) (less than)
  - [`gt`](./simd/gt.md) (greater than)
  - [`le`](./simd/le.md) (less than or equals)
  - [`ge`](./simd/ge.md) (greater than or equals)
- Integer Arithmetic
  - [`add`](./simd/i.add.md) (lane-wise add)
  - `sub` (lane-wise subtract)
  - `mul` (lane-wise multiply)
  - `dot` (lane-wise dot product)
  - `neg` (lane-wise negation)
- Extended Integer Arithmetic
  - `extmul` (extended multiplication)
  - `extadd` (extended pairwise addition)
- Saturating Integer Arithmetic
  - [`add_sat`](./simd/add_sat.md) (saturating add)
  - [`sub_sat`](./simd/sub_sat.md) (saturating subtract)
  - [`q15mulr_sat`](./simd/q15mulr_sat.md) (saturating Q-format rounding multiply)
  - [`min`](./simd/i.min.md) (select lane-wise minimum)
  - [`max`](./simd/i.max.md) (select lane-wise maximum)
  - [`avgr`](./simd/avgr.md) (lane-wise rounding average)
  - [`abs`](./simd/i.abs.md) (lane-wise absolute value)
- Bitwise Operations
  - `not` (bitwise not)
  - `and` (bitwise and)
  - `andnot` (bitwise and-not)
  - `or` (bitwise or)
  - `xor` (bitwise xor)
  - [`shl`](./simd/shl.md) (lane-wise shift left)
  - [`shr`](./simd/shr.md) (lane-wise shift right)
  - `bitselect` (bitwise select)
  - `bitmask` (bitmask extraction)
  - [`popcnt`](./simd/popcnt.md) (lane-wise population count)
- Boolean Horizontal Reductions
  - [`any_true`](./simd/any_true.md) (any bit not zero)
  - [`all_true`](./simd/all_true.md) (all lanes not zero)
- Floating Point Operations
  - [`neg`](./simd/neg.md) (lane-wise negation)
  - [`abs`](./simd/f.abs.md) (lane-wise absolute value)
  - [`min`](./simd/f.min.md) (NaN-propagating lane-wise select minimum)
  - [`max`](./simd/f.max.md) (NaN-propagating lane-wise select maximum)
  - [`pmin`](./simd/pmin.md) (lane-wise select psuedo-minimum)
  - [`pmax`](./simd/pmax.md) (lane-wise select psuedo-maximum)
  - `ceil`
  - `floor`
  - `trunc`
  - `nearest`
  - `demote`
  - `promote`

## Reference

- [`ref.null`](./reference/null.md)
- [`ref.is_null`](./reference/is_null.md)
- [`ref.func`](./reference/func.md)

## Parametric

- [`drop`](./parametric/drop.md)
- [`select`](./parametric/select.md)

## Variable

- [`local.get`](./variable/local.get.md)
- [`local.set`](./variable/local.set.md)
- [`local.tee`](./variable/local.tee.md)
- [`global.get`](./variable/global.get.md)
- [`global.set`](./variable/global.set.md)

## Table

- [`table.get`](./table/table.get.md)
- [`table.set`](./table/table.set.md)
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
- [`memory.size`](./memory/memory.size.md)
- [`memory.grow`](./memory/memory.grow.md)

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
