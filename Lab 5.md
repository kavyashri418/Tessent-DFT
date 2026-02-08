## IJTAG Implementation

_Objective: Understand how to create ICL & PDL files_

- Introduction: We have used a PLL design file for which .icl file will be created & .pdl file for the .icl file will be generated
- Set the context to DFT
  - This is done to set the primary context to DFT as .icl files are elaborated with the set_current_design
- Read the design source codes
  - This reads the design source code
- Elaborate the design top
  - The design files top has to be elaborated to make sure that the lower sub-modules are instantiated and integrated to the top module
- Create .icl file as per the syntax given:
  - <func>Port<port_name>;where<func>describes the function of the port such a DataInPort and <port_name> is the logical name you are assigning to the port
- Read the .icl file with a switch -force
  - This is going to read the .icl file such that tessent shell is aware of this file
- Elaborate the design top
  - The design file top has to be elaborated to make sure that the .icl file gets elaborated
- Create the .pdl file 
- Set the context to patterns
  - The primary context should be set to patterns and sub-context should be set to ijtag
- Set the design level to chip
- Verify the ICL ports
   - The Tessent shell will recognize the ICL ports
- Run DRC
- Create a PDL pattern set
  - The pattern set will define how the ports are driven with values

## DFT implementation process
```
Go to the directory - cd Tessent_labs
Run the dofile script
```

- To create .icl & .pdl files for a design
