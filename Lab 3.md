## Boundary Scan

_Objective: Understand how to insert Boundary scan at chip level_

- Introduction: There is a gate level circuit and few DFTs for which boundary scan needs to be implemented at chip level
- Instructions: The following instructions have been included in the script as comments
- Set the context to DFT
  - This is done to set the primary context to DFT as DFT instrument has to be inserted ie Boundary scan
- Create the TSDB directory
  - This directory is created automatically during DFT flow
- Read the cell library files
  - The I/O cell library needs to be read
- Read the design source codes
  - The RTL files needs to be read
- Read the design source codes
  - The RTL files needs to be read
- Elaborate the design up
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
- Set the design level to chip level
  - The boundary scan is always inserted at chip level
- Specify the DFT requirement
  - Here the boundary scan needs to be turned on
- Set attributes for the TAP controller pins
  - Here the attributes for the TAP controller pins(ie) TDI, TCK, TMS, TRST, TDO are specified
- Run the DRC
  - DRC ie design rule check is performed to validate the DFT requirements
- Create & report the DFT specification
  - After a successful DRC run, create DFT specification & report the same on the Tessent shell
- Insert the DFT instruments
  - This is going to insert the DFT components and a modified RTL file is created inside the TSDB directory
- Display the visualizer
  - This will display the added DFT components using the DFT visualizer

## DFT implementation process
```
Go to the directory - cd Tessent_labs
Run the dofile script
```

- To insert Boundary scan using Tessent shell at chip level

