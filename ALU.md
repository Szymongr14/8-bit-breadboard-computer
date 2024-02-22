# Arithmetic Logic Unit (ALU)

Implemented ALU can only add and subtract values stored in the A and B registers and send result to the bus. Subtraction is implemented by negating value stored in the B register (we change value to two's complement format by using XOR gates and adding one by carry input). We can switch between adding and subtracting by subtract signal (SU) on breadboard.

### Example of addition:
![](images/addition.png)

### Example of subtraction:
![](images/subtraction.png)

# Integrated circiuts used in this module

| id| type | amount |
|--|--|--|
| 74LS86 | 4x XOR gates | 2 |
| 74LS245 | 8-bit bus transceiver ( 8 tristate gates ) | 1 |
| 74LS283 | 4-bit binary adder | 1 |

**2x 74LS283** are used for doing operations on 8-bit values. **74LS245** is used for managing signal sent to the bus and **2x 74LS86** are used for changing vlaue stored in the B register to two's complement only when subtract signal is high.

# Schematic :
![](images/alu_schematic.png)