# interface_lcd_basic_v1
How to interface an HD44780 LCD with PIC16F690 in 8-bit mode.

RS (Register Select) determines if the data transfer between the display and 
the mcu are characters or a command/status. When the the mcu needs to send a command
to the display or to read the status, it must be pulled low. If character is to
be sent it needs to be high. (Refer to the datasheet for further display commands instructions)

The R/W pin determines in which way the data shall go. If low the command or
characters are beeing written to the display. When high the character data or command
from the display are being read.

The Enable pin initiates the actual data transfer. When writing to the display the 
data is transferred only on the high to low transition of the pin. 
 
