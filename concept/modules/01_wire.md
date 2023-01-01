# Module 01: Wires

This Module can have 3 to 6 wires, only one wire has to be cut. Here is the Setup-Table for the module. Notation is inspired by regex (use regexr.com to check it)

## Rules
```
wire-colors:
r=red, g=green, b=blue, w=white, y=yellow

0 no wire
^ not that color
* any wire
```

### 3 wires
| Rule No | Rule | Dip | regex | cut wire no | Valid Permutations
|-|-|-|-|-|-|
|1 | If there are no red wires, cut the second wire.|| not found yet |second|nc|
|2|Otherwise, if the last wire is white, cut the last wire.|||last|nc |
|3|Otherwise, if there is more than one blue wire, cut the last blue wire.|||last blue||
|4|Otherwise, cut the last wire.|||last||


### 4 wires
| Rule No | Rule | Dip | regex | cut wire no | Valid Permutations
|-|-|-|-|-|-|
|1|If there is more than one red wire and the last digit of the serial number is odd, cut the last red wire.|||last red||
|2|Otherwise, if the last wire is yellow and there are no red wires, cut the first wire.|||first||
|3|Otherwise, if there is exactly one blue wire, cut the first wire.|||first||
|4|Otherwise, if there is more than one yellow wire, cut the last wire.|||last||
|5|Otherwise, cut the second wire.|||second||


### 5 wires
| Rule No | Rule | Dip | regex | cut wire no | Valid Permutations
|-|-|-|-|-|-|
|1|If the last wire is black and the last digit of the serial number is odd, cut the fourth wire.|||fourth||
|2|Otherwise, if there is exactly one red wire and there is more than one yellow wire, cut the first wire.|||first||
|3|Otherwise, if there are no black wires, cut the second wire.|||second||
|4|Otherwise, cut the first wire.|||first||


### 6 wires
| Rule No | Rule | Dip | regex | cut wire no | Valid Permutations
|-|-|-|-|-|-|
|1|If there are no yellow wires and the last digit of the serial number is odd, cut the third wire.|||third||
|2|Otherwise, if there is exactly one yellow wire and there is more than one white wire, cut the fourth wire.|||fourth||
|3|Otherwise, if there are no red wires, cut the last wire.|||last||
|4|Otherwise, cut the fourth wire.|||fourth||


## setup of the module for playing
In Order to make it less obvious for the person who sets up the bomb which setting results in which wire to be cut, the manual for setup should include a list of valid setups with a valid dip configuration. The easiest way for the module to know which  wire should be cut would be to encode the wire-number with the dip switches and let it read which wires are connected uppon starting. But that would give the constructor the answer which wire should be cut. So I would vote against it.

Instead have a list of possible configurations stored in module memory. By setting the Dip-Switches you select which configuration should be needed. Uppon loading the module it should check whether it's physical configuration (which wire is connected) matches the required configuration set by the dip-switch. If not don't start the module instead set error.
