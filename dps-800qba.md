# DPS-800QB A Reverse Engineering

## Pinout

| pin | signal | pin | signal          |
|-----|--------|-----|-----------------|
| a1  | gnd    | b1  | gnd             |
| a2  | gnd    | b2  | gnd             |
| a3  | gnd    | b3  | gnd             |
| a4  | gnd    | b4  | gnd             | 
| a5  | gnd    | b5  | gnd             |
| a6  | gnd    | b6  | gnd             |
| a7  | gnd    | b7  | gnd             |
| a8  | gnd    | b8  | gnd             |
| a9  | gnd    | b9  | gnd             |
| a10 | gnd    | b10 | gnd             |
| a11 | gnd    | b11 | gnd             |
| a12 | gnd    | b12 | gnd             |
| a13 | gnd    | b13 | gnd             | 
| a14 | gnd    | b14 | gnd             |
| a15 | gnd    | b15 | gnd             |
| a16 | gnd    | b16 | gnd             |
| a17 | gnd    | b17 | gnd             |
| a18 | gnd    | b18 | gnd             |
| a19 | SDA    | b19 | A0              |
| a20 | SCL    | b20 | A1              |
| a21 | PSON   | b21 | +12V SB         | 
| a25 |        | b25 | chassis detect? |

Chassis detect needs to be ground before
PSON works.

## i2c/pmbus

```
i2cdetect -y 4
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:                         -- -- -- -- -- -- -- -- 
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
50: -- -- -- 53 -- -- -- -- -- -- -- 5b -- -- -- -- 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
70: -- -- -- -- -- -- -- --
```
