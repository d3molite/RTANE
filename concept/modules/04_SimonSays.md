# Simon Says
This module consists of four colored buttons, each with it's own LED.

## Rules
1. One of the four colored buttons will flash.
2. Using the correct table below, press the button with the corresponding color.
3. The original button will flash, followed by  another. Repeat this sequence in order using the color mapping.
4. The sequence will lengthen by one each time you correctly enter a sequence until the module is disarmed.

The matching color is dependent on the serial number of the bomb and how many strikes you've got.

## configuration
with the dip switches you can select a mode (out of the six possible) and a pattern

```
Switch    1   2   3   4   5   6   7   8  
Funct.  |   Mode    |     Pattern       |
```

Accepted Modes:
|Mode | Beschreibung |
|-|-|
|``0 0 1``| serial w/ vowels, no strikes |
|``0 1 0``| serial w/ vowels, 1 strike |
|``0 1 1``| serial w/ vowels, 2 strikes |
|``1 0 1``| serial /w vowels, no strikes |
|``1 1 0``| serial /w vowels, 1 strike |
|``1 1 1``| serial /w vowels, 2 strikes |
|``0 0 0``| invalid pattern |
|``1 0 0``| invalid pattern |

Patterns
|Pin | Function|
|-|-|
|4+5| Difficulty|
|6-8| Pattern|