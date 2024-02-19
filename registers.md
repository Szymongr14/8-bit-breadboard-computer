# Registers


Second step was to build two general purpose registers and instruction register. Registers of course are 8 bit wide, so they can store 256 different values.  Instruction register has 4 blue LEDs which indicate op-code of instrucion and 4 yellow LEDs  for operand of instruction. Op-code will be sent to the decoder so it's not connected to the bus.

### Register build in detail:

![](images/register_image.png)


# Integrated circiuts used in this module

| id| type | amount |
|--|--|--|
| 74LS173 | 4-bit register based on d flip flop | 6 |
| 74LS245 | 8-bit bus transceiver ( 8 tristate gates ) | 3 |

2x 4-bit registers are used to store value of each register LED's show content of register. To send only one value at the same time we need bus trensceiver with [tristate gates](https://www.learnelectronicswithme.com/2021/10/tristate-gates-and-buffers.html). They allow us to send data on specific signal. Only one register at once can send data to the bus. 

### Registers with the bus

![](images/all_registers.png)

### Schematic of a register
![](images/a-register.png)
