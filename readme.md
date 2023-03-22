
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
  - [`add`](./numeric/add.md) (addition)
  - [`sub`](./numeric/sub.md) (subtraction)
  - [`mul`](./numeric/mul.md) (multiplication)
  - [`div`](./numeric/div.md) (division)
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
  - [`trunc`](./numeric/f.trunc.md) (truncate / round toward zero)
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
  - [`extract_lane`](./simd/extract_lane.md) (get lane value)
  - [`replace_lane`](./simd/replace_lane.md) (set lane value)
- Comparisons
  - [`eq`](./simd/eq.md) (equals)
  - [`ne`](./simd/ne.md) (not equals)
  - [`lt`](./simd/lt.md) (less than)
  - [`gt`](./simd/gt.md) (greater than)
  - [`le`](./simd/le.md) (less than or equals)
  - [`ge`](./simd/ge.md) (greater than or equals)
- Integer Arithmetic
  - [`add`](./simd/i.add.md) (lane-wise addition)
  - [`sub`](./simd/i.sub.md) (lane-wise subtraction)
  - [`mul`](./simd/i.mul.md) (lane-wise multiplication)
  - [`dot`](./simd/dot.md) (lane-wise dot product)
  - [`neg`](./simd/i.neg.md) (lane-wise negation)
- Extended Integer Arithmetic
  - [`extmul`](./simd/extmul.md) (extended multiplication)
  - [`extadd`](./simd/extadd.md) (extended pairwise addition)
- Saturating Integer Arithmetic
  - [`add_sat`](./simd/add_sat.md) (saturating addition)
  - [`sub_sat`](./simd/sub_sat.md) (saturating subtraction)
  - [`q15mulr_sat`](./simd/q15mulr_sat.md) (saturating Q-format rounding multiplication)
  - [`min`](./simd/i.min.md) (select lane-wise minimum)
  - [`max`](./simd/i.max.md) (select lane-wise maximum)
  - [`avgr`](./simd/avgr.md) (lane-wise rounding average)
  - [`abs`](./simd/i.abs.md) (lane-wise absolute value)
- Bitwise Operations
  - [`not`](./simd/not.md) (bitwise not)
  - [`and`](./simd/and.md) (bitwise and)
  - [`andnot`](./simd/andnot.md) (bitwise and-not)
  - [`or`](./simd/or.md) (bitwise or)
  - [`xor`](./simd/xor.md) (bitwise xor)
  - [`shl`](./simd/shl.md) (lane-wise shift left)
  - [`shr`](./simd/shr.md) (lane-wise shift right)
  - [`bitselect`](./simd/bitselect.md) (bitwise select)
  - [`bitmask`](./simd/bitmask.md) (bitmask extraction)
  - [`popcnt`](./simd/popcnt.md) (lane-wise population count)
- Boolean Horizontal Reductions
  - [`any_true`](./simd/any_true.md) (any bit not zero)
  - [`all_true`](./simd/all_true.md) (all lanes not zero)
- Floating-point Operations
  - [`neg`](./simd/f.neg.md) (lane-wise negation)
  - [`abs`](./simd/f.abs.md) (lane-wise absolute value)
  - [`min`](./simd/f.min.md) (NaN-propagating lane-wise select minimum)
  - [`max`](./simd/f.max.md) (NaN-propagating lane-wise select maximum)
  - [`pmin`](./simd/pmin.md) (lane-wise select psuedo-minimum)
  - [`pmax`](./simd/pmax.md) (lane-wise select psuedo-maximum)
- Floating-point Arithmetic
  - [`add`](./simd/f.add.md) (addition)
  - [`sub`](./simd/f.sub.md) (subtraction)
  - [`div`](./simd/f.div.md) (division)
  - [`mul`](./simd/f.mul.md) (multiplication)
  - [`sqrt`](./simd/f.sqrt.md) (square root)
  - [`ceil`](./simd/ceil.md) (ceiling / round up)
  - [`floor`](./simd/floor.md) (floor / round down)
  - [`trunc`](./simd/trunc.md) (truncate / round toward zero)
  - [`nearest`](./simd/nearest.md) (round to nearest)
- Conversions
  - [`convert`](./simd/convert.md) (convert `i32` to floating-point)
  - [`trunc_sat`](./simd/trunc_sat.md) (convert floating-point to `i32` with saturation)
  - [`demote`](./simd/demote.md) (convert `f64` to `f32`)
  - [`promote`](./simd/promote.md) (convert `f32` to `f64`)
  - [`narrow`](./simd/narrow.md) (integer narrowing)
  - [`extend`](./simd/extend.md) (integer extension)

## Reference

- [`ref.null`](./reference/null.md) (place a null reference on the stack)
- [`ref.is_null`](./reference/is_null.md) (check if a reference is null)
- [`ref.func`](./reference/func.md) (place a `funcref` on the stack)

## Parametric

- [`drop`](./parametric/drop.md) (drop the top value from the stack)
- [`select`](./parametric/select.md) (conditionally select an operand)

## Variable

- [`local.get`](./variable/local.get.md) (push local variable to stack)
- [`local.set`](./variable/local.set.md) (pop stack value and write to local variable)
- [`local.tee`](./variable/local.tee.md) (write top of stack to local variable without pop)
- [`global.get`](./variable/global.get.md) (push global variable to stack)
- [`global.set`](./variable/global.set.md) (pop stack value and write to global variable)

## Table

- [`table.get`](./table/table.get.md)
- [`table.set`](./table/table.set.md)
- [`table.size`](./table/table.size.md)
- [`table.grow`](./table/table.grow.md)
- [`table.init`](./table/table.init.md)
- [`elem.drop`](./table/elem.drop.md)
- [`table.copy`](./table/table.copy.md)
- [`table.fill`](./table/table.fill.md)

## Memory

- [`load`](./memory/load.md) (load a value from memory and place it on the stack)
- [`store`](./memory/store.md) (store an operand to memory)
- [`memory.size`](./memory/memory.size.md) (get the total size of memory)
- [`memory.grow`](./memory/memory.grow.md) (request more memory)
- [`memory.init`](./memory/memory.init.md)
- [`data.drop`](./memory/data.drop.md)
- [`memory.copy`](./memory/memory.copy.md)
- [`memory.fill`](./memory/memory.fill.md)

## Control

- [`unreachable`](./control-flow/unreachable.md)
- [`nop`](./control-flow/nop.md)
- [`block`](./control-flow/block.md)
- [`loop`](./control-flow/loop.md)
- [`if`](./control-flow/if.md)
- [`else`](./control-flow/else.md)
- [`end`](./control-flow/end.md)
- [`br`](./control-flow/br.md)
- [`br_if`](./control-flow/br_if.md)
- [`br_table`](./control-flow/br_table.md)
- [`return`](./control-flow/return.md)
- [`call`](./control-flow/call.md)
- [`call_indirect`](./control-flow/call_indirect.md)
