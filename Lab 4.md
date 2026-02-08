## Scan Chain Insertion

_Objective: Understand how to insert scan chain into a design_

- Introduction: Use a block level design called tracking_channel that has a single instance of a sub-module called code_gen
- Both tracking_channel and code_gen are RTL designs that have gone through previous DFT insertions steps to insert EDT into the RTL. The RTL for both of these designs was synthesized into a single file gate  design with all the sequential elements mapped to scan equivalent cells

- Set the context to DFT with the sub-context to scan
  - This is done to set the primary context to DFT & sub-context to scan as DFT instrument has to be inserted ie scan cells
- Create the TSDB directory
  - This directory is created automatically during DFT flow
- Read the cell library files
  - The I/O cell library needs to be read
- Read the synthesized design
  - The gate-level netlist file needs to be read
- Load designs files from the TSDB directory
- Elaborate the design top
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
- Run the DRC
  - DRC ie design rule check is performed to validate the DFT requirements
- Set a chain constraint for scan chain
  - It is going to set the scan chain as per the count given and FFs will be distributed depending upon the no of chains
- Distributed the scan elements to chain
  - This will distribute the FFs on the chain
- Report the distribution prior to insertion
  - Reports the scan chain & cells
- Modify the netlist
  - Insert the test logic
- Review the report files

## DFT Implementation Process
```
Go to the directory - cd Tessent_labs
Run the dofile script
```

- To insert the scan chain in a single mode for a given design
