# sky130PLLdesign
PLL design done through VSD IAT sky130PLLdesign workshop
!!! PLEASE NOTE THAT THIS REPO WILL CONTAINS ONLY BASIC KNOWLEDGE OBTAINED FROM THIS WORKSHOP, SIMULATION SCREENSHOTS AND IN DETAIL ANALYSIS IS TO BE EXPECTED VERY SHORTLY !!!

## Part 1: Introduction to PLL

In egineering practise there are two main ways to generate clock signal for digital design, those are using quartz crystal and voltage controlled oscillators.
Main goal of our PLL is to create clock gnerating system with good properties of both approaches (stability of crystal and flexibility of voltage controlled oscillator).
Basic PLL components include following:
Voltage Controlled Oscillator
Phase Frequency Detector
Charge Pump
Low Pass Filter
Frequency Divider
	
## Part 2: Introduction to Phase Frequency Detector

Phase Frequency Detector is component of PLL whose output depends on difference of output and referent signal. It has two outputs, UP and DOWN and depending on wheteher they are of the same phase and freqnecy UP and DOWN signal set their value to instruct rest of system to speed UP or speed DOWN output signal so it matches referent signal.

PFD can be designed using two negative edge triggered flip flops and one AND gate. Such design is simple and reliable but followed with one big problem, so called Dead Zone (minimum amount of difference of output and reference which can be detected). Further development efforts should be aimed solving that issue.

## Part 3: Introduction to Charge Pump

Charge Pump has sole purpose to interpret UP and DOWN control signals from previous stage in order to create analog voltage level which should be forwarded to VCO.
Charge Pump can be made using two current sources and one capacitor on the output (for smoothening output value). As addition, Charge Pump needs Low Pass Filter in order to ensure its stability.


## Part 4: Introduction to Voltage Controlled Oscillator and Frequency Divider

Voltage controlled oscillator is an oscillator whose frequency can be adjusted by changing control signal/voltage.
In IC technology, Ring oscillators are very simple to create. Accoring to that, it is very important to notice that regular ring oscillator (composed of odd number of inverters) can be easily modified to become VCO. It is achieved to putting control logic to its current supply so that we can change frequency by starving oscillator with current.

Frequency divider is also very simple design and it consists of toggle flip flop.

Before we conclude PLL theory, lets bring up some terms closely related to PLL design:
Lock range: Range of frequencies for which PLL is able to keep in locked state (assuming that PLL is in locket state)
Capture Range: Range of Frequencies which PLL can lock onto (assuming it is not in locked state)
Settling Time: Time within PLL is able to lock from unlocked state

## Part 5: Tool Setup and Design Flow

Tools setup process is straightforward:
For installing Ngspice (tool for simulation of circuits) following comand should be used:
sudo apt-get install ngspice
For Installing Magic (tool for layout design, design rule check, parasitic extraction etc) following commands should be used:
sudo apt-get update && sudo apt-get upgrade
git clone git://opencircuitdesign.com/magic
sudo apt-get install csh
cd magic
./configure
make
sudo make install

## Part 6: Introduction to PDK, specifications and pre-layout circuits

TO BE DONE

## Part 7: Circuit design simulation tool - Ngspice Setup

TO BE DONE

## Part 8: Layout design tool - Magic Setup

TO BE DONE

DAY 2, TO BE DONE AS WELL
