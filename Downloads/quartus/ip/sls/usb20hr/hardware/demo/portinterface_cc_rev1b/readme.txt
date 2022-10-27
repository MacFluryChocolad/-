 //***********************************************************
 //                    System Level Solutions, Inc.
 //                    e-mail: support@slscorp.com
 //                        www.slscorp.com
 //***********************************************************
 //***********************************************************
 //
 // Author       : SLS
 //
 // File         : ReadMe.txt
 //
 // Date         : 13/04/2009
 //
 // Description:  This ReadMe file contains the following information:
 //            
 //                   - Information regarding demonstration of port interface application
 //                     of usb20hr with ulpi interface.
 //
 //
 //************************************************************

 // Follow steps as given below for performing demonstration
 //=============================================================
 
  -->Steps for loading Port Interface system on CoreCommander Cyclone III(3C25) Board Rev1b.
 
     1> Connect USB Blaster on J1 port(JTAG) of the board.
     2> Connect USB2.0 compliant cable into USB mini connector(CON2) on board
     3> Switch on the board.
     4> Detect the USB blaster into PC.
     5> Run portinterface.bat file from this folder, Just double click on it and detect sls usb2.0     
        device into USBVIEW.
     6> It will show USB_ATTACHED, USB_RESET, USB_SUSPEND and etc.. message at JTAG console which
        shows USB event occurs at hardware level.
     
  -->Steps for running port interface application
     
     1> Run Portinterface application from the following path <USB20HR Installation Path>
        \software\ 
        utilities\portinterface.
     2> Perform single word read/write or word verify or file read/write operation between 
        location
        (1)   0x02100000 to 0x021FFFFF
   
Note:- for getting more information about port interface application please refer ReadMe.txt file
       from the following path <USB20HR Installation Path>\software\ utilities\portinterface.
        
 