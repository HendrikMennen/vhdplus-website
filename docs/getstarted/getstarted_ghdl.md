---
id: ghdl
title: Simulate your program
sidebar_label: GHDL Simulation
---


> :warning: _This section is a work in progress._

[GHDL and GTKWave](/docs/getstarted#addional-programs) is required to use the simulator.

In order to help with finding errors and not always have to program the FPGA, you can simulate your program. 
You can set the inputs of Main or a Component to trigger an operation and after running the simulation, you can see how the values of all signals change while running the code. This way, you have a lot of information to compare at a glance, which helps to find the error or check if your code works as expected.

Here is an example on how to use the simulation:
<div class="fluidMedia"><iframe id="ytplayer" type="text/html" width="100%" src="https://www.youtube.com/embed/Jmq_wjdd9wM?autoplay=0&origin=http://vhdplus.com" frameborder="0" allowFullScreen></iframe></div>

# How to Simulate Your Code

## Install the required programs

1. Click on Extras/Package Manager
2. Install GTKWave and GHDL

## Create the simulation file

### Simulation Assistant

1. Open the file to simulate
2. Click on the button with the pulse symbol or click on Tools/Simulation
3. Make sure the correct file is selected
4. Set the time to simulate (don't set the time too high, or the simulation will take a long time to finish)
5. Set "CLK Frequency" to the frequency of the clock that is connected with the CLK input
6. Select the inputs of the simulated component. You can then emulate the input like when the inputs are used in the final FPGA
7. Click on Save

### Emulate the inputs

#### Visual

1. Select the input to emulate
2. Set the time for that the input should have a value
##### When the data is '1' or '0':
1. Click on the rising or falling edge button
##### When you have an individual value:
1. Set the value the input should have
2. Click on the plus symbol
##### When you want to repeat the value sequence (e.g. for a clock signal)
1. Set the data to repeat (e.g. 1ms '1', 1ms '0')
2. Click on the repeat button

#### Code

With the code you can emulate the inputs. 
Programming the `.ghdp` file is like with `.vhdp`, but with some changes. 
For example:
- `wait for ...;` adds a delay between the operations before and after
- `wait;` stops process
- `wait until ...;` waits until condition is true

There are much more tools that you can use for the simulation, but the best way is to just search for "VHDL Simulation". The same operations for VHDL work with GHDP as well.

## Start the simulation

1. Click on the run symbol in the simulation bar
2. Check for errors in the output window
3. After GTK Wave is open, click on the component of which you want to see the signal
4. Double click the signal to display in the wave window
5. You can zoom out and see the simulated behavior

# Simulation with VHDL

1. Write your VHDL simulation code
2. Right click on the VHDL file
3. Select "Simulate with GHDL"