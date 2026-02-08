## EDT IP Creation

_Objective: Understand how to insert EDT IP core using Tessent Test-kompress_

- Introduction: starting with a gate level netlist, a non-scan netlist, insert scan chains using Tessent scan, create Tessent Test-kompress EDT IP core
- Set the context to DFT scan mode
  - This is done to set the primary context to DFT & sub-context to scan mode for scan insertion
- Read the cell library files
  - The I/O cell library needs to be read
- Read the synthesized design
  - The gate-level netlist file needs to be read
- Set the current design for elaboration process
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
  - If any module descriptions are missing, design elaboration will identify them by adding add_black_boxes-auto
- Identify and define control signals
- Run DRC
- Set the scan chains count to 2
- Insert the scan logic
- Report scan chains and new test logic
- Write the scan inserted netlist
  - It creates the scan chain netlist inside the netlist directory
- Write out atpg dofile and testproc file
  - The following instructions have been included in the script edt_ip.do as comments.
- Set the context to DFT edt mode
  - This is done to set the primary context to DFT & sub-context to edt mode for EDT ip insertion
- Read the scan chain netlist
- Read the cell library files
  - The I/O cell library needs to be read
- Set the current design for elaboration process
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
- Define scan chains & control signals
- Used to run the Tcl procedure from the atpg.do
- Specify parameters for EDT logic
- Report EDT channels & pins
- Run DRC
- Report configuration of EDT logic
- Report required lock-up cells
- Write the EDT modified RTL

## DFT Implementation Process
```
Go to the directory - cd Tessent_labs
Run first the dofile.do script followed by edt_ip.do script
```

- To insert an EDT IP core into a scan stitched netlist
