<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This project uses four input pins (A, B, C, D) and represents a 4-bit BCD code. This BCD code is then converted with just NAND gates to a 4-bit excess-3 code at the output pins (W, X, Y, Z), as shown in the following truth table.

|    | A | B | C | D |   | W | X | Y | Z |
|----|---|---|---|---|---|---|---|---|---|
| 0  | 0 | 0 | 0 | 0 |   | 0 | 0 | 1 | 1 |
| 1  | 0 | 0 | 0 | 1 |   | 0 | 1 | 0 | 0 |
| 2  | 0 | 0 | 1 | 0 |   | 0 | 1 | 0 | 1 |
| 3  | 0 | 0 | 1 | 1 |   | 0 | 1 | 1 | 0 |
| 4  | 0 | 1 | 0 | 0 |   | 0 | 1 | 1 | 1 |
| 5  | 0 | 1 | 0 | 1 |   | 1 | 0 | 0 | 0 |
| 6  | 0 | 1 | 1 | 0 |   | 1 | 0 | 0 | 1 |
| 7  | 0 | 1 | 1 | 1 |   | 1 | 0 | 1 | 0 |
| 8  | 1 | 0 | 0 | 0 |   | 1 | 0 | 1 | 1 |
| 9  | 1 | 0 | 0 | 1 |   | 1 | 1 | 0 | 0 |
| 10 | 1 | 0 | 1 | 0 |   | x | x | x | x |
| 11 | 1 | 0 | 1 | 1 |   | x | x | x | x |
| 12 | 1 | 1 | 0 | 0 |   | x | x | x | x |
| 13 | 1 | 1 | 0 | 1 |   | x | x | x | x |
| 14 | 1 | 1 | 1 | 0 |   | x | x | x | x |
| 15 | 1 | 1 | 1 | 1 |   | x | x | x | x |

## How to test

Just test every 16 BCD code combinations and look if the output corresponds to the above truth table.

## External hardware

For the inputs, any buttons, switches or DIP switches are sufficient. To check the output, a 7-segment display or dedicated LEDs can be used. All hardware found on the Tiny Tapeout development board. So, there's no need for additional hardware.
