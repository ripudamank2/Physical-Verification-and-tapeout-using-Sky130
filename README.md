# Physical-Verification-and-tapeout-using-Sky130

Physical verification is the process in which a circuit design and its layout works as planned. Steps include design rule checking (DRC) and layout-versus-schematic (LVS) checks.





### Table of Content
#### DAÝ 1: Introduction to SkyWater SKY130
    A. Open_pdks
    1. SkyWater PDK
    2. Open tool setups
    3. Libraries
    4. 3rd-party packages
    5. Projects
    B. Understanding the Skywater PDK
    1. Layers
    2. Rules
    3. Devices
    4. Libraries
        i. Digital standard cells
        ii. I/O cells
        iii. Primitive devices
    C. A Simple manual design flow
    1. Creating schematics
    2. Creating device layouts
    3. Simulating the netlist
#### Lab 1:
    A. Open_pdks installation
    1. Installing open_pdks and the SkyWater PDK
    2. Project setup best practices
    3. Setting up for layout with magic
    4. Setting up for schematic capture with xschem
    5. Setting up for LVS with netgen
    B. Creating a SKY130 device layout in magic
    C. Creating a simple schematic in xschem
    D. Exporting a schematic to layout
    E. Simulating the netlist
-----------------------------------------------------
#### DAY 2: Introduction to DRC and LVS
    A. Understanding GDS format
    1. Streaming format
    2. Layer:Purpose pairs
    3. Hierarchy
    4. Some tools/scripts for manipulating GDS
    B. Understanding extraction and SPICE formats
    1. Running extraction
    2. ngspice
    3. Extraction styles and options
    4. ext2spice options
    5. Extraction for LVS
    6. Parasitic extraction
    7. Full R-C extraction
    C. GDS reading and writing in magic
    1. Readonly option
    2. Flatten options
    3. Hierarchy & magic's database
    4. Polygon subcells
    5. Library option
    6. Addendum option
    7. Noduplicates option
    8. Working with GDS styles
    9. GDS special purpose styles
    D. DRC rules in magic
    1. Interactive DRC in magic
    2. DRC vs. correct-by-design in magic
    3. DRC rules hidden by hierarchy
    4. DRC rules in the tech file
    5. DRC verification layouts
    E. Extraction rules in magic
    1. Extraction styles
    2. Device types
    3. Hierarchical extraction
    4. DRC errors uncovered by extraction
    F. LVS setup for netgen
    1. Setup options
    2. Device description
    3. SPICE vs. SPICE
    4. SPICE vs. verilog
    5. Black-boxing
    G. Verification by XOR
    1. ECO
    2. XOR
#### Lab 2:
    A. Basic GDS:
    1. Reading/writing GDS to/from magic
    2. GDS compositing with magic
    3. Vendor GDS
    4. Reading unknown GDS (magic and klayout)
    5. GDS read/write options
    B. Basic extraction:
    1. Extracting a SPICE netlist from magic
    2. Extraction options
    3. Parasitic extraction
    
    C. Setup for DRC:
    1. Running magic (on a prepared example)
    2. Using DRC styles
    3. Using alternative tech files
    4. Running sign-off scripts
    5. Viewing DRC in klayout
    D. Setup for LVS
    1. Netgen setup scripts
    2. Running netgen (on a prepared example)
    E. Setup for XOR
    1. Creating an ECO (from a prepared example)
    2. Running XOR
---------------------------------------------------------
#### DAY 3: Front-end and back-end DRC
    A. Back-end (metal layer) rules
    1. Width
    2. Spacing, Notch
    3. Wide-spacing
    4. Minimum Area
    5. Via overlaps
    6. Minimum hole
    7. Slot rules
    8. Via generation rules
    B. Local Interconnect
    C. Front-end rules
    1. Transistor rules
    2. Implants, ID layers, Boundary layers
    3. Wells, Same-net rules
    4. Deep N-well
    5. High voltage rules
    6. Resistors
    7. Capacitors
    8. Diodes
    9. Fixed-layout devices
    D. Miscellaneous rules
    1. Off-grid errors
    2. Restricted angles
    E. Latchup rules
    F. Antenna rules
    G. Stress rules
    H. Density rules
    1. Why density rules?
    2. Layer density requirements
    3. Fill generation algorithm
    4. Fill blocking
    5. When automation fails
    G. Recommended rules
    1. Double vias
    H. DRC in Magic:  DRC styles
    I. Dumping and viewing DRC results
    J. Fixing DRC errors
#### Lab 3:
    A. Running Magic's interactive DRC
    B. Running antenna checks
    C. Running Magic's batch DRC
    D. Running the fill generation script
    E. Running the density checker script
    F. Checks with alternative tech files
    G. Catching violations by extraction
---------------------------------------------------------
#### DAY 4: Understanding PNR and physical verification
    A. openlane/OpenROAD automation
    B. Avoiding DRC violations
    i. Local interconnect rules
    ii. Density planning
    iii. Latchup rules
    C. SRAM
    D. Managing hard macros
    E. Top-level routing
    F. Manually fixing violations
#### Lab 4:
    A.OpenLANE labs
---------------------------------------------------------
#### DAY 5: Running LVS
    A. Generating netlist from schematic
    B. Generating LVS netlist from layout
    C. Differences between LVS netlists and simulation netlists
    D. How to prepare netlists for both simulation and LVS
    E. Verilog vs. layout
    F. Running netgen
    G. Pre-match analysis
    H. Hierarchical checking and flattening
    I. Property checking
    J. Pin checking
    K. Series/Parallel combining
    L. Symmetry breaking
    M. Interpreting results
    N. Fixing errors
#### Lab 5:
    A. Creating a (simple) hierarchical circuit in schematic
    B. Exporting a schematic to netlist
    C. Importing a schematic netlist into layout
    D. Exporting a circuit layout to netlist
    E. Creating a (simple) hierarchical circuit in verilog
    F. Running LVS
    G. Interpreting LVS results
    H. Fixing LVS errors
