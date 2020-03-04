# Lab 5: Binary counters

The purpose of this laboratory exercise is to become familiar with the creation of sequential processes in VHDL, to implement clock enable signal to drive another logic with slower clock, and to design a binary counter. We will use a push button on the CoolRunner board as reset device, onboard clock signal with frequency of 10&nbsp;kHz for synchronization, and 7-segment display as output device.


#### Contents

1. [Materials](#1-Materials)
2. [Synchronize Git and create a new folder](#2-Synchronize-Git-and-create-a-new-folder)
3. [Clock enable VHDL code](#3-Clock-enable-VHDL-code)
4. [Binary counter VHDL code](#4-Binary-counter-VHDL-code)
5. [Top level implementation of 4-bit counter](#5-Top-level-implementation-of-4-bit-counter)
6. [Clean project and synchronize git](#6-Clean-project-and-synchronize-git)


## Preparation tasks (done before the lab at home)

1. Calculate how many periods of clock signal with ![equation](https://latex.codecogs.com/gif.latex?f_%7Bclk%7D%20%3D%2010%5C%2C%5Ctext%7BkHz%7D) contain time intervals 10&nbsp;ms, 250&nbsp;ms, 500&nbsp;ms, and 1&nbsp;s. Write values in decimal, binary, and hexadecimal forms.

    &nbsp;
    
    ![equation](https://latex.codecogs.com/gif.latex?T_%7Bclk%7D%3D%5Cfrac%7B1%7D%7Bf_%7Bclk%7D%7D%3D%200%2C1%20ms)
    
    &nbsp;

    | **Freq** | **Time** | **Number of periods** | **Number of periods in binary** | **Number of periods in hexa** |
    | :-: | :-: | :-: | :-: | :-: |
    | 100&nbsp;Hz | 10&nbsp;ms |  |  |  |
    | 4&nbsp;Hz | 250&nbsp;ms |  |  |  |
    | 2&nbsp;Hz | 500&nbsp;ms |  |  |  |
    | 1&nbsp;Hz | 1&nbsp;sec |  |  |  |

2. See how to create a [synchronous operation](https://github.com/tomas-fryza/Digital-electronics-1/wiki/VHDL-cheat-sheet#processes) in the VHDL.
