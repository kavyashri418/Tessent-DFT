## Memory BIST

_Objective: Understand the DFT flow for inserting MBIST_

- Introduction: There is a block B which is a single level of hierarchy which has a memory instance ie memA. clkB is the functional clock for block B
- Instruction: The following instructions have been included in the script as comments.
- Set the context to DFT
  - This is done to set the primary context to DFT as DFT instrument has to be inserted ie MBIST
- Create the TSDB directory
  - This directory is created automatically during DFT flow
- Read the cell library files
  - The I/O cell library needs to be read
- Read the design source codes & memory files
  - The RTL & memory files needs to be read
- Elaborate the design top
  - The design files top has to be elaborate to make sure that the lower sub modules are instantiated and integrated to the top module
- Set the design level to sub-block level
  - The memory block to which MBIST is inserted is a sub-block
- Specify the DFT requirement
  - Here the MBIST needs to be turned on and a clock needs to be added for the MBIST
- Verify the DFT requirement
  - DRC ie design rule check is performed to validate the DFT requirements
- Create & report the DFT specification
  - After a successful DRC run, create DFT specification & report the same on the Tessent shell
- Display the DFT specification
  - This is going to open the GUI interface of the DFT visualizer and you will see the specification as IJTAG network & MBIST
- Insert the DFT instruments
  - This is going to insert the DFT components and a modified RTL file is created inside the TSDB directory
- Display the visualizer
  - This will display the added DFT components using the DFT visualizer
- Extract the ICL
  - This will generate the .icl (Instrument Connectivity Language), .pdl (Procedural Description Language), .sdc (Synopsys Design Constraint) files
- Create & report the pattern specification
  - This will create the pattern specification & report the same
- Process the patterns
  - This will generate the patterns needed for simulation
- Set up the simulation library
  - This will set the simulation libraries needed for testbench simulations
- Run & check the simulation
  - This will validate the IJTAG & MBIST insertions

## DFT implementation process:
```
Go to the directory: cd Tessent_labs
Run the dofile script
Observe the output
```

- To insert the MBIST at sub-block level using Tessent DFT flow
