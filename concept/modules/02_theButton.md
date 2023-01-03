# Module 01: Wires

This Module consists of one large button and a colored lights strip next to it. You need to be able to see the main timer module while operating this module.

## Rules
The action needed to be performed consits of two phases, pushing and releasing. Either you need to push and immediately let go or you need to push and let go in the precise moment any digit of the main timer shows one of the noted numbers.

1. If the button is blue and the button says "Abort", hold the button and refer to "Releasing a Held Button".
2. If there is more than 1 battery on the bomb and the button says "Detonate", press and immediately release the button.
3. If the button is white and there is a lit indicator with label CAR, hold the button and refer to "Releasing a Held Button".
4. If there are more than 2 batteries on the bomb and there is a lit indicator with label FRK, press and immediately release the button.
5. If the button is yellow, hold the button and refer to "Releasing a Held Button".
6. If the button is red and the button says "Hold", press and immediately release the button.
7. If none of the above apply, hold the button and refer to "Releasing a Held Button".

__Releasing a Held Button__

If you start holding the button down, a colored strip will light up on the right side of the module. Based on its color, you must release the button at a specific point in time:
- Blue strip: release when the countdown timer has a 4 in any position.
- White strip: release when the countdown timer has a 1 in any position.
- Yellow strip: release when the countdown timer has a 5 in any position.
- Any other color strip: release when the countdown timer has a 1 in any position.

## construction of the module
The button must be colorless transparent to be illuminated from below via adressable LEDs. There should be a possibility to insert a transparent sheet with the text printed on. The color light strip should be illuminated by adressable LEDs too.

Needed Button-Colors are:
- blue
- white
- yellow
- red

Needed Button-Texts are:
- Abort
- Detonate
- Hold

For added confusion some other colors (e.g. green, orange, pink) and labels (e.g. Release, Push, Pull) should be provided.

The light-strip needs to show:
- blue
- white
- yellow
- any other color (eg. red, green, purple)

## Interconnect to bomb core
There are two ways this module could interact with the bomb core.

Method 1 doesn't need a data bus but requires the bomb core to be aware of the module, it's slot and its required sequence. So the module would just need to know which sequence needs to be performed (push/release or push/hold/release). If the appropriate sequece is excecuted, the module sets itself to deactivated. The bomb core then needs to check on the second sequence type whether the release was performed during the correct digit.

Method 2 does need the data bus but doesn't need the bomb core to know where this module is and which sequence is needet. The bomb core will transmit each second the timestamp and the module checks wheter it's the right sequence, then it pulls the appropriate control-line. This would also allow the use as a needy module