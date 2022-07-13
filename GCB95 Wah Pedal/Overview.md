# Project Overview
This project is to mod a gcb95 crybaby pedal.
<p align="center">
<img src= "Photo%20Dump/open_chassis.jpg" width = "400">
</p>
The guitar pedal is found [here](https://www.long-mcquade.com/123/Guitars/Guitar-Effects/Dunlop/Original-Cry-Baby-Wah.htm). There are numerous sources online that can explain what this pedal is, so read those if interested as this project is not meant to cover that information. Instead, this will cover modifications being made to this pedal.

The pedal itself has a circuit incorporated that is 'non true bypass' meaning that when the pedal is off, a buffer circuit inside is still connected between the circuit input and output causing what is known as 'tone suck' to a guitar pedal chain. A pedal chain is just a series of guitar pedals connected that work to create
a unique sound for the effects that a guitar player will create when connected to it. Tone suck is bad as it means that even when a pedal is turned
off, part of the guitar sound will be affected by the pedal, and sometimes causes the overall sound to not be what is desired simply from having this
circuit present in the chain.

A common mod is known as a 'true bypass' mod. This mod essentially skips this buffer circuit or 'bypasses' it, so that the signal in the guitar effect chain goes directly from pedal input to output, thus not allowing any of the buffer circuit to influence the rest of the guitar pedal chain when the pedal is turned off.

This was one of the mods done to the pedal. Another mod was to change the effect type of the pedal itself. The gcb95 is a wah pedal but a simple circuit modification transforms it into a volume pedal instead. A wah pedal is basically an envelope filter effect the gives a guitar a funky sound, like what Jimi Hendrix would often use. A volume pedal is much simpler, as the name suggests, it adjusts the volume of the signal chain. Both these effects serve their purpose so there is a desire to have the ability to use both.

The mods done are:
- True Bypass
- Volume/Wah combination
- (To be done later) Toggle switch between buffered (non-True Bypass) and unbuffered (True Bypass)

## Details on mods
### True Bypass
This mod was created following directions as given by [instructions found here](https://www.electrosmash.com/crybaby-gcb-95), [here](https://stinkfoot.se/archives/546), and [here](http://www.danieleturani.com/howto-and-diy/convert-crybaby-wah-pedal-to-true-bypass/). 
I also did not like having no feedback for when the pedal is engaged as there is no native led on the pedal chassis. So, in addition to this mod, I added an led to turn on when the Wah effect was engaged. This mod was done by adding a led with an appropriately sized resistor connected to the input power and ground lines.

### Volume
The volume mod was found to be very simple, it just involved removing a single capacitor on the circuit as explained [here](https://www.instructables.com/Modify-Your-Wah-Pedal/). I'm also very greedy, why would I just want to have a volume pedal or wah pedal, why can't I have both? I can! Instead of simply removing this capacitor, I also added a switch with an led to indicate when the capacitor was connected or open circuited (removed). That way I can toggle between both effects. 

### Reality
Unfortunately, I learned that based on the design of this pedal, the volume mod is not perfect. While it does work, the effective range is not 100%. What I mean is that when the pedal is rocked from up to down, the radius of motion is not 100%, this means that the while Wah effect works well, since this was a Wah pedal originally so duh, with the volume pedal mod active, the volume does not go to absolutely zero. Even so, this is a fun thing to have and is still very much usable.
