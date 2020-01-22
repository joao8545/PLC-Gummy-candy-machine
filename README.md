# PLC-Gummy-candy-machine

[![Languages](https://img.shields.io/badge/Language-XSOFT--CoDeSys-blue?style=plastic)]()

## Statement of the problem

The problem is to implement an automation of a gummy candy machine (Figure 1). Used software: CoDeSys (LD).

Gummy candy machine operation starts by the press of Start (NO contact) pushbutton and stops at any time by Stop (NC contact) pushbutton press. During the operation green indicator lamp should light permanently.

The raw components from three basic (jelly, colourant, flavour) raw material tanks goes to the mixing tank through magnetic valves. PLC controls opening/ closing of all magnetic valves. The machine has to mix a gummy candy. Filling of the raw components starts with 4 s delay after the press of Start pushbutton, Raw materials filling is carried out sequentially: the jelly is filling for 5 s, the colourant for 2 s, the flavour for 3 s.

The mixing motor starts to mix mixture of raw components with 2 s delay after the moment when all necessary raw materials are in the mixing tank (the raw material filling stage is finished). Mixing stage is carried out as follows: 2 s delay - 4 s clockwise rotation 2 s delay - 4 s anticlockwise rotation.

After mixing the drain magnetic valve is necessary to open with 2 s delay. The level-switch indicates if the tank is empty. Magnetic valve is needed to keep opened for 5s after level-switch indication. Then the drain magnetic valve must be closed and the mixing process is finished.

The level switch output signal is a short pulse, which the programmer simulates by an NO contact pushbutton press. Programmer actuates it during the simulation.

Candy mixing can be restarted by Start pushbutton repress.

## PLC Contacts

In the table below there is the relation of the PLC input and the variable name

PLC Input | Variable name
------------ | -------------
Start Pushbutton | Start_PB
Stop Pushbutton | Stop_PB
Level Switch | Level_SW


In the table below there is the relation of the PLC output and the variable name

PLC Output | Variable name
------------ | -------------
Operation Lamp | OpLamp
Jelly Magnetic Valve | Red_V
Colourant Magnetic Valve | Blue_V
Flavour Magnetic Valve | Green_V
Drain Magnetic Valve | Drain_V
Clockwise Contactor | Right_C
Anticlockwise Contactor | Left_C

## Solution implementation


![PLC_VISU](https://github.com/joao8545/PLC-Gummy-candy-machine/blob/master/Visu.PNG)


In the image above there is a proposed visualization for the problem. There it is possible to follow al the elapsed time in each TON and also see the state of each PLC output.
