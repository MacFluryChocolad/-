Altera RLDRAM II and QDRII/II+ Controller with UniPHY v9.1

 

Although we have made every effort to ensure that this version
of the Altera(R) software functions correctly, there may be
problems that we haven't encountered. If you have a question or
problem that is not answered by the information provided in
this readme.txt file, please contact Altera support at 
1-800-800-EPLD or submit a Service Request at mysupport.altera.com.
 
User guide:

The QDR II and QDR II+ SRAM Controller and RLDRAM II Controller with UniPHY User Guides give full information on using 
these two products.

The user guides are on the External Memory Handbook webpage, http://www.altera.com/literature/lit-external-memory-interface.jsp
 

Usage:

 
You must run the IPTCL_MOD_NAME_pin_assignments.tcl script after Quartus II Analysis and Synthesis has completed
successfully and before Quartus II Fitting.  This script automatically finds all the top level pins and applies the appropriate 
constraints to them.  The script should be run whenever top level pin names have changed.  Old or user modified assignments
are removed before new assignments are added.  


PLL/DLL Sharing:

The PLL master option can be used to export the clock signals from a "master" controller for use by an 
identical "slave" controller.  A typical use case would involve generating a single master controller, multiple
slave controllers and using the PLL and DLL outputs from the master to drive the inputs on the slaves.  The connection
from master to slaves can be made using a user-written wrapper RTL file (when using Megawizard Plug-in Manager) or 
with the SOPC Builder.  This configuration only works correctly if the master and slaves have all been configured 
identically (other than the PLL/DLL sharing option).

Timing Simulation:

Timing simulation is not supported for Stratix III and Cyclone III devices.  Timing simulation support is preliminary
for Stratix IV and Arria II GX devices.

 
Using Only the PHY:

The /IPTCL_MOD_NAME/IPTCL_RTL_DIR/IPTCL_MOD_NAME_memphy_top.v contains just the PHY portion with the parameter defaults
set to the appropriate values given the current parameterization.  This module can be used directly with a 
custom controller.  The interface conforms to the AFI specification.


Adding Memory Device Presets

There is no fully supported flow to add presets.  However, additional presets can be added manually by editing 
the /ip/altera/uniphy/lib/altera_uniphy_rldramii.qprs or the /ip/altera/uniphy/lib/altera_uniphy_rldramii.qprs.  


Bus Turnaround Time:

Bus turnaround is not timing analyzed. Consequently, the controller "dead times" are based on assumptions about the user 
board trace lengths.  For timing analysis to be correct, board trace delays must be limited to 0.6 ns from FPGA 
to memory and from memory to FPGA.


Directory Structure:

IPTCL_MOD_NAME.v (or .vhd)
IPTCL_MOD_NAME.qip
/IPTCL_MOD_NAME/
            IPTCL_RTL_DIR/
            IPTCL_CONSTRAINTS_DIR/
            IPTCL_EXAMPLE_DIR/
            IPTCL_RTLSIM_DIR/
            IPTCL_TIMINGSIM_DIR/

IPTCL_MOD_NAME.v

This is the top level RTL which defines the Uniphy controller and phy.  

IPTCL_MOD_NAME.qip

This file contains references to all of the required RTL, constraints and TCL scripts required to compile the Uniphy controller 
and phy.  This is the only file which should be added to the project, if not done so automatically.

IPTCL_RTL_DIR

Contains all of the Verilog RTL which implements the IPTCL_MOD_NAME parameterization of the UNIPHY core.  Included are the PHY 
and controller which communicate using the AFI 2.0 protocol.  


IPTCL_CONSTRAINTS_DIR

Contains a number of Tcl scripts, a Pin Planner File (.ppf) and an .sdc file.


IPTCL_EXAMPLE_DIR

Contains a Quartus II example design complete with an example traffic generator.  This design is ready to compile and can be used 
as an example of how to instantiate, constrain and interface with the UNIPHY core.  Also included in a generic memory model.


IPTCL_RTLSIM_DIR

Contains a testbench that can be used for functional simulation.


IPTCL_TIMINGSIM_DIR

Contains a testbench which can be used for timing accurate simulation.
 



