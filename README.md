# 8-bit-up-down-counter
8-bit synchronous up/down counter in VHDL with reset, enable and direction control, simulated in Xilinx Vivado.
# 8-Bit Up/Down Counter (VHDL)

A synchronous 8-bit up/down counter written in VHDL and verified with a
testbench in Xilinx Vivado (behavioral simulation).

## Features
- 8-bit output `y[7:0]`
- Synchronous active-high reset
- Enable input to start/pause counting
- Direction select `m`: `0` = count up, `1` = count down
- Wraps around on overflow/underflow (255 -> 0 and 0 -> 255)

## Ports
| Port   | Dir | Description                          
|--------|-----|--------------------------------------|
| clk    | in  | Clock (rising edge)                  |
| reset  | in  | Synchronous reset, active high       |
| enable | in  | Counting enabled when '1'            |
| m      | in  | Direction: '0' up, '1' down          |
| y      | out | 8-bit count value                    |

## Files
- `up_down_counter.vhd` - counter design (entity `countr`)
- `countr_tb.vhd` - testbench

## Simulation
1. Open the project in Vivado.
2. Run Simulation -> Run Behavioral Simulation.
3. Set `y` radix to Unsigned Decimal and run for ~500 ns.

The testbench covers reset, count up, count down, hold (enable low)
and a second reset.

## Tools
VHDL, Xilinx Vivado
