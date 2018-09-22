# Multiple Blink
The purpose of this code is to blink 2 LEDs on a board at different rates. The boards used for this were the msp430g2553 and the msp432p401r.


# G2
To make 2 LEDs blink at different rates, first the ports for the LEDS are established for P1.0 and P1.6. Utilizing variable i set at 50,000 with a decrementor function, the modulus function was used to create different rates of toggling with one variable. For the Green LED, the modulus function was set to 30,000, so whenever variable i was divisiable evenly by 30,000, the LED would toggle. For the Red LED, the modulus function was set to 10,000, which would generate a different toggle rate than the green LED. 

# P401R
The code used for the P401R is almost exactly the same as the G2 code, except changing the which ports used. With P1.0 remaining the same for the Green LED and P1.6 changing to P2.1 for the Red LED.
