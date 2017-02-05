InterStellarGadget
==================

A simple modification to Gadget-2.0.7 (available from [here](https://wwwmpa.mpa-garching.mpg.de/gadget/)) that adds some things that are useful for non-cosmological simulations of single galaxies in a separate environment. Currently this adds

+ A fixed dark matter potential based on a NFW profile.
+ A custom equation of state based on the work of Martizzi (2016).

This is implemented through the following compiler options:

+ DFIXED\_POTENTIAL: switches on the fixed potential
+ DNO\_SELF\_GRAVITY: removes all self gravity (it is still calculated, though, so this does not offer any considerable speedup -- this should be fixed in the future)
+ MARTIZZI\_EOS

You will need to add the following things in your paramter file (we sugguest using the initial conditions generator [here](https://www.github.com/JBorrow/GoGoGadget)):

For Martizzi EOS:

+ f\_Martizzi
+ F\_Martizzi
+ P\_fin -- note this must be simulation units
+ fgas

For fixed NFW:
+ R\_nfw
+ HaloMass
+ c\_nfw
