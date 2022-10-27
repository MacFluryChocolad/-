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
 // Date         : 05/07/2008
 //
 // Description:  This ReadMe file contains the following information:
 //            
 //                   - Information regarding demonstration of Streaming(write operation) application
 //                     of usb20hr with ulpi interface.
 //
 //
 //************************************************************

 // Follow steps as given below for performing demonstration
 //=========================================================
 
  -->Steps for loading Streaming Application system on CoreCommander Cyclone III(3C25) Board Rev1b.
 
     1> Connect USB Blaster on J1 port(JTAG) of the board.
     2> connect USB2.0 compliant cable into USB mini connector(CON2) on board.
     3> Switch on the board.
     4> Detect the USB blaster into PC.
     5> Run streaming_bo.bat file from this folder, Just double click on it
        and detect sls usb2.0 device into USBVIEW.
     
  -->Steps for running streaming application
     
     1> Run Streaming application from <USB20HR Installation Path>\software\
        example\windows\rwusb_csharp\rwusb\bin\release.
     2> Perform Bulk Out operation as per application console
         
     
 
   Note:- for performing BULK OUT operation write number of bytes from streaming application.