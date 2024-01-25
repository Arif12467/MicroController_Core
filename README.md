# 8-bit MicroController Core [WIP]
## Arif Amzad

## About
In this Project, a Fully Custom 8-bit MicroController Core was created using an IBM 90nm Process Design Kit (PDK). The MicroController Core can be controlled by a 6-bit instruction where instruction<0:2> execute the Op-Code and instruction<3:5> are used to control the memory instance or the shift amount. The core consisted of a Full-Adder, Logarithmic Shifter, Shift Enable Logic Circuit, an 8x8 SRAM Array, Programmable Logic Array (PLA), Level Sensitive Latch, 3-to-1 Multiplexer, and a Bus Driver (Tristate). Each component was designed and tested to ensure maximum speed and signal integrity. Layouts were made for each component to be used in the final assembly. This document shows the final layout of the entire MicroController Core. 

## Op-Code
| Assembly | Instruction<0:2> | Description                       |
|----------|------------------|-----------------------------------|
| NOP      | 000              | Do Nothing                        |
| LOAD     | 001              | Mem[i]<-External Bus              |
| STORE    | 010              | External Bus<-Mem[i]              |
| GET      | 011              | Accumulator<-Mem[i]               |
| PUT      | 100              | Mem[i]<-Accumulator               |
| ADD      | 101              | Accumulator<-Accumulator+Mem[i]   |
| SUB      | 110              | Accumulator<-Accumulator-Mem[i]   |
| SHIFT    | 111              | Left logical shift of Accumulator |

The table above provides a description of actions executed when the Programmable Logic Array is load with the Op-code

## Schematic
![This is an image](Schematic.png)

## Floorplanning
![This is an image](Floorplan.png)

This image showns the floorplan for the entire core and where each layout of individual circuit components can be found.

## Layout
![This is an image](Microprocessor.png)

Full Layout of 8-bit MicroController Core

## Verification
![This is an image]()

Clean DRC Check

![This is an image]()

Clean LVS Check

Note: Decoupling Capacitors are responsible for the small warning.
