# c099-surveyer 

Some RTK Survey scripts for the C099-F9P Modem 

Basically to facilitate using two modules as a base/receiver. 

Requires python3, pyserial for the command-line programs. For GUI, requires matplotlib and py-gobject (gi). 

Moreover, the mbed3 firmware needs to be installed on the ODIN-W2 (this is the default factory configuration!) 


If everything is configured properly on the base/rover (see doc) then you can use rover-cli or rover-gui. Rover-cli takes the serial port name as position argument. 


## Detailed usage guide: 

See doc/usage-guide.md . This will only work if someone (perhaps you) has set up the base/rover app appropriately. 


## setting everything up 

For now, follow the instructions doc/setup-guide.md 

In the future, it is planned to add some scripts to automatically set up the base/rover given their serial ports.  

## 3-D Printed Enclosure

To give your CO99-F9P some protection, you can use the Freecad project file/STL files in the enclosure directory. 


