# The Bomb core


## connection of the modules
Each module is connected to the bomb core via a multipin connector. Type and Position aren't decided yet. Preference goes to Buchsenleiste 2x5 [1] or Wannenstecker [2]. As latter are designed to accept the counterpart on a flat cable and not from a pcb, voting tends to lean to the first.

### Pinout

|Pin|Function|
|-|-|
|1|+5V|
|2|Module Defused|
|3|Module Strikes|
|4|nc|
|5|RS-485 Tx+|
|6|RS-485 Tx-|
|7|RS-485 Rx+|
|8|RS-485 Rx-|
|9|nc|
|10|GND|


## Transmitting the state of a module
In Rev. 1 the modules only transmit there current state by pulling ``Pin 2`` or ``Pin 3`` HIGH to show the respective state. The Core-Checker has 22 Digital In to read these states (either Arduino Mega (or simmilar) or with IO Expansion). It connects to the timer / Display-Module where the state of the bomb is shown and the game is started, stopped and reset.

In Rev. 2 a more elaborate communication-scheme is planned where the modules talk to the bomb core to tell them their configuration and read data from other modules. So it can now in which state any other module is. This will be done on a RS-485 4wire Bus. Bus-Master is the bomb core, all modules (including Timer) are slaves and read the bus, listen to messages designated for them and reply after being queried by bomb core. A strike and the defusing will still be transmitted via dedicated pins to be faster and backwards compatible.


## weblinks
Example. Don't need to buy there

[1] https://www.reichelt.de/buchsenleisten-2-54-mm-2x05-gerade-mpe-094-2-010-p119929.html?&trstct=pol_26&nbc=1

[2] https://www.reichelt.de/wannenstecker-10-polig-gerade-wsl-10g-p22816.html?&nbc=1&trstct=lsbght_sldr::225087