# PLC-Gummy-candy-machine
##Implementation of an automation problem in CoDeSys

The problem is to implement an automation of a gummy candy machine (Figure 1). Used PLC:Eaton Easy822-DC-TC or EC4P-200. Used software: EasySoft 6 (LD) or CoDeSys (LD or FBD or
ST).Gummy candy machine operation starts by the press of Start (NO contact) pushbutton and stops
at any time by Stop (NC contact) pushbutton press. During the operation green indicator lamp
should light permanently.The raw components from three basic (jelly, colourant, flavour) raw material tanks goes to the
mixing tank through magnetic valves. PLC controls opening/ closing of all magnetic valves. The
machine has to mix a gummy candy. Filling of the raw components starts with 4 s delay after the
press of Start pushbutton, Raw materials filling is carried out sequentially: the jelly is filling for 5 s,
the colourant for 2 s, the flavour for 3 s.The mixXing motor starts to mix mixture of raw components with 2 s delay after the moment
when all necessary raw materials are in the mixing tank (the raw material filling stage is finished).
Mixing stage is carried out as follows: 2 s delay - 4 s clockwise rotation 2 s delay - 4 s
anticlockwise rotation.After mixing the drain magnetic valve is necessary to open with 2 s delay. The level-switchindicates if the tank is empty. Magnetic valve is needed to keep opened for 5s after level-switch
indication. Then the drain magnetic valve must be closed and the mixing process is finished.The level switch output signal is a short pulse, which the programmer simulates by an NOcontact pushbutton press. Programmer actuates it during the simulation.Candy mixing can be restarted by Start pushbutton repress.
