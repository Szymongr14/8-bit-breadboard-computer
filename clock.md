# Clock module
The first step in making a fully functioning 8-Bit computer is making the clock module. The clock is a square wave at 50% duty cycle.

![](images/clock_image.png)

- - -
#### Clock works in two modes: 
- **automatic** with changeable speed
- **manual** which allow to pulse only one clock cycle by pushing button (helpful to troubleshoot and debug)

Modes are changed by slide switch. 


# Integrated circiuts used in this module

| id| type | amount |
|--|--|--|
| NE555 | clock signal with SR Latch | 3 |
| 74LS04 | 6 NOT gates | 1 |
| 74LS08 | 4 AND gates | 1 |
| 74LS32 | 4 OR gates | 1 |

First NE555 is used to generate main clock signal, next two are used to debounce signal while using manual mode and switching between modes. Logic gates are used to connect it all together and have access to halt clock signal.




# Schematic
![](images/clock_schematic.png)


Building this module was actually my first contact with breadboards so wiring is not perfect. 
