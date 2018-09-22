# Simple Blink
The purpose of these programs is to get an LED on a MSP430 board to blink at an even rate, where 50% of the time it is off, and 50% of the time it is on. The boards used for these were the MSP430G2553 board and the MSP430F5529 board. 

## G2
On the G2, utilizing the msp430g2553 header makes assigning the ports easier, as the full binary can be replaced with the simpler hexidecimal. After disabling the watchdog timer, port 1.0 was set in the output direction as to be used in the math function which would toggle it on and off.  In said math function, an arbitrary value i was set at 50,000 and was set up to count down 1 per cycle. Port 1 output was toggle with an OR statement, so that if it was on, it would turn off, and vice versa. After that took place, a delay of 50,000 cycles would begin, afterwards the program would begin anew, and toggle Port 1 bit 0 again.

![](https://media.giphy.com/media/7NXqEhQMQdpeZWxD9w/giphy.gif)

## F5229
On the F5229, utilizing the msp430f5229 header, the code remains relatively unchanged due to the necessary ports needed to emulate a blinking LED shared the same funciton between the boards. 

![](https://media.giphy.com/media/Zva3vGcysHIGx70Ydv/giphy.gif)
