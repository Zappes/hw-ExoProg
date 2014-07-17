Programmer breakout board for ATtiny85
======================================

What Is this?
-------------
When I use an ATtiny85 instead of an ATmega328, I do so because I want to save space on the PCB. This normally means that I omit the ISP header which makes working on the software a little tricky - I have to do all the programming on a breadboard or I have to remove the chip from the PCB, program it using an external programmer and then re-insert it into the circuit. Quite a pain, actually.

The ExoProg is a little board that contains an ATtiny85 and two 4:2 multiplexer ICs. There also is a second 8-pin socket which is connected using a simple cable to the socket in the actual circuit. The last connector is an ISP header to which a programmer can be connected. Normally, the pins of the microcontroller are simply connected to the pins of the second socket, so the ExoProg doesn't really do anything - it's just like an ATtiny85 on a wire.

As soon as the reset pin of the ATtiny is pulled low, though, the multiplexers cut the connection between the ISP pins of the ATtiny and the external circuit and connect the microcontroller's ISP pinbs to the programmer header. This makes it possible to program the ATtiny without interfering with the actual circuit at all - the multiplexers make sure that the ISP signals are completely isolated from the external circuit.

