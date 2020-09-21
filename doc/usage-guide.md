# Preliminaries

This document assumes that the base/rover boards have been configured appropriately. If they haven't yet, see setup-guide.md. 

For a working system, we need to C099-F9P boards, one acting as a "base" and
one acting as a "rover." Both receive GPS signals, and the base sends
information about the signals it receives the rover via WiFi, which the rover
can then use to deduce the relative position between its antenna and the bases antenna. 

When the rover has a solution for the relative position, it sends it out via
its serial port. The programs here provide a way to log out the relative
positions. 


# Running Configuration 


The base needs to be turned on first (by applying power), so that the rover can
connect with it. You can use the Reset (RST) buttons on the Base/Rover to make
them start over, but you'll always want to reset the base first so the rover
has something to connect to. 

When the base and rover have a GPS fix, a blue light will start flashing. When
the rover is talking to the base, a purple LED will be on (possibly flashing).
When the rover has a solution for the relative position, a yellow LED will appear. 

Only the rover needs to be plugged into the receiving computer via USB. In
fact, it's easiest if the base is not, because that makes it easier to figure
out what serial port needs to be used to talk to the Rover. 



# The GUI 


# The CLI 







