# Button Blink
The purpose of this code is to create a virtual switch with a button turning on an LED. The boards used for this were 

# G2
To create a switch that turns on an LED with a button, multiple ports are required, with P1.3 being the button to activate the LED, and P1.0 being the output direction that the LED is on.  A mux of P1SEL is used to detect if P1.3 is sending a bit to the LED. Within the if statement, the & statement of P1IN and BIT3 is checked by the mux, and if it returns a value of 0, the LED will turn on. The else statement being the LED is off, allowing the button to control the LED directly.

![](https://media.giphy.com/media/lcTbTOkaWssj97N1SB/giphy.gif)

# FR2311
The FR2311 needed to be designed differently than the G2, as it did not have a P1SEL to utilize. After arranging the ports for the board for the button (P1.1), and the output direction (P1.0), the GPIO high impedence mode is disable to use previous port settings. The if statement is modified from the G2 iteration, with an AND statement between P1IN and BIT1 to activate the LED. The issue with this setup is that the button is subject to contact bounce, in that one press may result in multiple outputs. 
