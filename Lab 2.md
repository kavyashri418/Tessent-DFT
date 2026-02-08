## Clock and DRC

_Objective: Understand what could be DRC violations for MBIST_

- Introduction: There is a physical block that contains two instances of block A and one instance of block B. The physical block also includes a clock divider, a clock mux and clock gaters. There will be DRC violations that will need to be fixed

- Instructions: The following instructions have been included in the script as comments.
- Set the context to DFT
  - This is done to set the primary context to DFT as DRCs are checked in the DFT flow
- Read the cell library files
  - The I/O cell library needs to be read
- Read the design source codes
  - The RTL files needs to be read
- Read the TSDBs of the sub-blocks
  - The TSDBs of the sub-blocks to be opened
- Elaborate the design top
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
- Source the PDL file of the clock divider
  - The .pdl file won't be automatically elaborated unlike the .icl file, hence needs to be sourced
- Report the open TSDB directories
  - This will display the list of TSDB directories
- Report the name & location of the tsdb directories
  - This will display the location of tsdb directories
- Report IJTAG instances that are included in this design
  - This will display the ijtag instances
- Report all the ICL modules
  - This will display the .icl modules loaded into the design
- Report the identified clock enables
  - It will report the clock enable point of the clock gaters
- Set the design level to physical block level
  - The memory blocks are part of a core block now
- Specify the DFT requirements
  - Here the MBIST needs to be turned on without adding clock so that the DRC violations will be observed
- Verify the DFT requirements
  - DRC ie design rule check is performed to validate the DFT requirements
- Report a specific DRC violation
  - DRC violation errors about a specific violation can be reported
- Analyze the violation using schematic viewer
  - DRC violation errors can be viewed in GUI mode using DFT visualizer
- Fixing the violation DFT_C1-1
  - DRC violations are fixed
- Run the DRC
  - DRC ie design rule check is performed to validate the DFT requirements
- The above process is repeated till all the violations are fixed
- Report the clocks
  - All the clocks will be defined now
 
## DFT implementation process
```
Go to the directory - cd Tessent_Labs
Run the dofile script
Observe the output
```

- To fix DRC violations at physical block level in a MBIST environment
