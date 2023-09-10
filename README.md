# IHCsetup
Setup of my IHC controller V1



## Mac OS connection
having a ust to serial cable / dongle, You can access the IHC by adding a straight through DSUB 9 female - female cable.

You can run the following commands:


```
ls -l /dev/tty.* /dev/cu.*

The tty entry is for reading, while we here will use the cu entry for the usb to serial thingy.

Then run 

screen /dev/cu.usbserial-1410 115200 cs8 ixoff

to exit screen again:

c-a c-\
``` 
https://apple.stackexchange.com/questions/32834/is-there-an-os-x-terminal-program-that-can-access-serial-ports

https://pbxbook.com/other/mac-tty.html

https://apple.stackexchange.com/questions/168401/how-can-i-redirect-the-output-of-screen-to-a-file



Exit does not wotk:

use ctrl-a ctrl-d (detach)

screen -list

and then 
screen -X -S 30766 quit
