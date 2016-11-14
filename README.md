# ledCube8x8x8
cube of 512 LEDS that can show amazing animations using 8 bit atmega 32 MCU at a frame rate of 1300/s

documented pdf can be found here https://drive.google.com/open?id=0BxDy0M91HFancmhxUG1wZmJwaDVSMGd1X0NWRmF4QzdnLWlV 

have a look at how awesome this project looks :D

https://www.youtube.com/watch?v=3B742fAvcUM

coded in Atmel Studios 7 for Atmega 32 set of MCu.. just change the main.c 

for eg.-// you will be using atmega 32 and the interrupt values are as follows prescalar of 128 OCR value 10

pseudo code as follows-

TCCR2 |= (1 << CS20) | (1 << CS22) | (1 << WGM21); 
TIMSK |= (1 << OCIE2); OCR2 = 10;

giving u (16 MHz / 128 (prescalar) / 11 (ocr value) / 8 ) = 1420.45 times cube refreshed per second . (where after 8 interrupts complete cube gets refreshed).

Modes are-
wave form generation mode..
clear on time compare mode ..
and use a 16 bit timer too..

                     - Kartik Nighania
