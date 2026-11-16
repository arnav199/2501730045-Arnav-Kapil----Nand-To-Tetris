# Capstone: Make the Computer Draw a Box

Nand to Tetris – I (ETCCNT301), K.R. Mangalam University
Name: Arnav Kapil · Roll no.: 2501730045 · **K = 1**

The Hack computer shows a black box while any key is pressed, and clears it when the key is released.

## Files (`capstone/`)

| File | What it is |
| --- | --- |
| `CPU.hdl`, `Memory.hdl`, `Computer.hdl` | Part A: the Hack computer |
| `assembler.py` | Part B: two-pass Hack assembler in Python |
| `Box.asm` | Part C: the box program in Hack assembly |
| `Box.hack` | `Box.asm` assembled with `assembler.py` |

## My K

- Box starts at row 1, is 20 rows tall and 16 × ((1 mod 4) + 1) = 32 pixels (2 words) wide, from the left edge.
- Assembler extra feature (K mod 3 = 1): a wrong line prints a message with its line number (for example `Line 7: invalid instruction`) instead of crashing.

## How to run

Assemble the box program:

```
python capstone/assembler.py capstone/Box.asm
```

This writes `capstone/Box.hack`. Load it in the CPU Emulator, run it, and hold down a key.

For Part A, put the three `.hdl` files in the same folder as the lab chips, load each official `.tst` file in the Hardware Simulator, and run it.
