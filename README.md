## Half Adder

A half adder adds two 1-bit inputs and produces a sum and a carry.

| A | B | Sum | Carry |
|---|---|-----|-------|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |

- Sum = A XOR B
- Carry = A AND B

**Files:** `src/half_adder.v`, `tb/half_adder_tb.v`

**Run:**
​   bash
iverilog -o sim src/half_adder.v tb/half_adder_tb.v
vvp sim
gtkwave half_adder.vcd
<img width="1080" height="695" alt="half_adder_waveform" src="https://github.com/user-attachments/assets/0884f91c-5e8f-4242-8778-7754b76329c8" />

## Simulation (QuestaSim)

vlib work
vlog src/half_adder.v tb/half_adder_tb.v
vsim -voptargs=+acc work.half_adder_tb
add wave -r /*
run -all
