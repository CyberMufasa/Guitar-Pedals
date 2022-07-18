# LEDS
For the leds included, resistors must be chosen appropriately that support the expected current draw based on color.
I based the resistance values on the standard current draws for each led color based on [listed specs from sparkfun](https://www.sparkfun.com/products/9590#:~:text=A%20must%20have%20for%20power,rated%20forward%20current%20of%2020mA)

[hrtr]
(https://www.sparkfun.com/products/11372#:~:text=It%20has%20a%20typical%20forward,rated%20forward%20current%20of%2030mA)
red - 20mA
blue - 30mA

The resistances were calculated using the standard voltage formula V=IR -> R=V/I leading to:
Red: R = 9V/20mA = 450 Ohm
Blue: R = 9V/30mA = 300 Ohm
I did not have those exact values so a combination of resistors in placed in series was used from what I had available. As long as they are close to the above values, it is fine. It must not be less, but more is good, I may even increase what I did use as the brightness is a little high for my liking.

# Switches
The switches chosen were to be 3PDT format with nine lugs to have room to also include the leds. This article provides a good explanation on what they are and how they work.
https://www.coda-effects.com/2015/03/3pdt-and-true-bypass-wiring.html

This is the exact set and model that I bought:
https://www.amazon.ca/gp/product/B07547HKMQ/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1

 I always got confused on which orientation the toggle action actually changed (which set of 3 lugs connect to the middle set when pressing the switch), I used my DMM to measure the connection to determine which set of 3 pins would short circuit (be connected) when I pressed this switch.

The existing switch in the Wah pedal appears to be this one from visual inspection:
https://www.jimdunlop.com/on-off-double-pole-double-throw-large-switch-d-logo-mxr-cry-baby/

Both sides if this switch in my pedal had the toggle points soldered together while other models I saw from pictures and videos did not. This appears to not actually matter, the only thing that comes to mind on why mine is different is that during manufacture, they were likely taken in bulk and soldered together for other purposes and one of these was placed in my pedal since it was available.

# The mods
I followed the directions outlined on the websites linked earlier for the circuit setup.
At first, I wanted to only add the led and do the volume/wah mod but after seeing how simple the true bypass mod is, I decided I may as well do it too.

# Procedure

	1. The first step was to determine how the switches would actually be introduced into the circuit along with connecting the led indicator for on/off toggle. I simply followed what was outline here:
	http://www.danieleturani.com/howto-and-diy/convert-crybaby-wah-pedal-to-true-bypass/ for where to add the connections to the PCB. In my setup, I took the 9V power directly to one of the two 3PDT switches middle lugs, then from one of the side lugs in the same row to the led which had the resistors calculated earlier in series, back to the PCB to the ground point close to where the 9V power was taken. 
	
	For the 'effect' circuit to be connected to this same 3PDT switch, I took out the 4.7uF capacitor, shown in https://www.instructables.com/Modify-Your-Wah-Pedal/, and soldered a new capacitor to a small perf board. The positive side of where the capacitor was originally in the PCB had a wire soldered on to it, taken to a different center lug on the 3PDT switch, and one side lug in that same row went to the positive end of capacitor on the perfboard, and the negative end of the capacitor on this perfboard went to the negative terminal of the original position of the capacitor on the PCB. The other side lug in this same row on the 3PDT switch was left as open circuit, which is doing the same thing as if removing this capacitor as outline in the linked website. The leds return path is connected on the side lug of the 3PDT switch with the open circuit so that it turns on when the switch 'lifts' the capacitor or open circuit the connection engaging the 'volume' mode of the pedal. 
	
	NOTE: I did break one of the legs of the original capacitor, so I needed to use a new one. It was noted that the original was rated for 100V which I learned is actually not very common for that size. After some research, it appears that most guitar pedals will reach maybe 30V if they are consuming a ton of voltage. I found capacitors of that size were commonly only rated for 50V and used that instead since the above explanation implies it is a cross within the bounds of the expected circuit operation.
	
	2. The second mod was the true bypass mod as indicated by http://www.danieleturani.com/howto-and-diy/convert-crybaby-wah-pedal-to-true-bypass/. The circuit layout including the LED was replicated as exactly outlined in the website. Where the same led power and return path used in the other mod was used, and the contents of that buffer circuit were completely removed. 
	
Future plans are to put the components removed from this buffer circuit on the same perfboard as the capacitor with a switch added and connected back into the connection on the pcb where the true bypass components were removed to allow a toggle between buffered and true bypass modes.
