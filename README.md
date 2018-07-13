# interface_lcd_basic_v1
How to interface an HD44780 LCD with PIC16F690 in 8-bit mode using C as programming language.
The program has been written in C using MPLAB X IDE v4.00 and the XC8 compiler.

About the LCD-pins
RS (Register Select) determines if the data transfer between the display and 
the mcu are characters or a command/status. When the the mcu needs to send a command
to the display or to read the status, it must be pulled low. If character is to
be sent it needs to be high. (Refer to the datasheet for further display commands instructions)

The R/W pin determines in which way the data shall go. If low the command or
characters are beeing written to the display. When high the character data or command
from the display are being read.

The Enable pin initiates the actual data transfer. When writing to the display the 
data is transferred only on the high to low transition of the pin. 
 
Pin 1 Vss             GND-pin
Pin 2 Vdd             Power supply for logic
Pin 3 Vo              Operating voltage for LCD
Pin 4 RS              Register Select (described above)
Pin 5 R/W             Read/Write (descibed above)
Pin 6 E               Enable pin (described above)
Pin 7 - 10 DB0-DB03   Four low order bi-directional three-state data bus line (not used in 4-bit mode)
Pin 11 - 14 DB04-DB07 Four high order bi-directional three-state data bus line (DB07 can be used as busy flag)
Pin 15 A              Power supply for LED backlight (+)
Pin 16 K              Power supply for LED backlight (-)
