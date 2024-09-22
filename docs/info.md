<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

wokwi project using a D-flop ring to display "E_fab" in 7-seg dsiplay.

## How to test
On every clock pulse, display a letter in the repeating sequence "EFAB".

## How to test

Start with all input switches off,
and sliding switch to the left
(i.e. to select the automatic clock pulse).
The letter "F" should blink with every clock pulse.

Switch on input switch 3, and "E" should start blinking.

Switch on input switch 1, and it should then cycle through "EFAb".

Switch on input switch 8, and letter blinking should be disabled.

## Notes

These are the inputs:

| In  | Signal | Function                           |
|-----|--------|------------------------------------|
| SW1 | `IN0`  | **Run**: Off = Reset; On = Run     |
| SW2 | `IN1`  | (Unused)                           |
| SW3 | `IN2`  | `state_init[0]`; Normally ON       |
| SW4 | `IN3`  | `state_init[1]`; Normally off      |
| SW5 | `IN4`  | `state_init[2]`; Normally off      |
| SW6 | `IN5`  | `state_init[3]`; Normally off      |
| SW7 | `IN6`  | (Unused)                           |
| SW8 | `IN7`  | **Blink control**: On = no blink   |

`state_init` specifies the initial state for the sequencing
flip-flops during reset, and for normal operation the first (SW3)
would be switched ON, and the other three (SW4..6) would be
switched off.


## External hardware

none.
