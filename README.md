# RTLtoGDS-project
### Project summary 
Universal Shift Register Design
The design includes two Verilog modules:
**universal_shift_register_1bit**: Implements a 1-bit universal shift register.
**usr_nbit**: Instantiates the universal_shift_register_1bit module to create an N-bit universal shift register. The parameter size can be adjusted to define the bit-width of the register. In this example, a 4-bit universal shift register is implemented.
Synthesis and Physical Design Using** OpenLane**
The OpenLane flow was used for the synthesis and physical design of the usr_nbit module. The steps include:
**Preparation**: Setting up the PDK (Process Design Kit) and standard cell library.
**Synthesis**: Using **Yosys and abc** tools for generating the gate-level netlist and performing static timing analysis with OpenSTA.
**Floorplanning**: Defining core and die areas, placing I/O pads, and creating power distribution networks.
**Placement**: Determining the exact locations for standard cells within the core area.
**Clock Tree Synthesis (CTS)**: Ensuring uniform clock signal distribution to minimize skew and latency.
**Routing**: Interconnecting the cells with metal layers and vias, ensuring design rules are met.
**Verification**: Extracting SPEF for post-route STA, running DRC (Design Rule Check), LVS (Layout vs. Schematic), and generating GDS II files.
**Key Metrics**
Area: Chip area of usr_nbit is 251.491200 µm².
Cell Count: 23 standard cells of various types (buffers, flip-flops, inverters, etc.).
Wire Length: Total wire length after routing is 934 µm.
Vias: 266 vias were used for inter-layer connections.
Timing Analysis: Hold time and setup time analyses confirmed timing constraints were met, with sufficient slack.
