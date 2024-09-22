<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

A 4-bit arithmetic logic unit (ALU) is a device that can perform a variety of arithmetic and logic operations on two 4-bit operands.

## How to test

### Input

IN0       clk
IN1..IN3  operation type [3 bit] (see below)
IN4..IN7  operand value [4 bit]

### Output

OUT0..OUT3  value stored in the accumulator [4 bit]
OUT4..OUT6  unused (todo: zero, overflow flags)
OUT7        carry flag

## External hardware

none.
