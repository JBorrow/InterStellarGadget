InterStellarGadget
==================

A simple modification to Gadget-2.0.7 (available from [here](https://wwwmpa.mpa-garching.mpg.de/gadget/)) that adds some things that are useful for non-cosmological simulations of single galaxies in a separate environment. Currently this adds

+ A fixed dark matter potential based on a NFW profile.

This is implemented through the following compiler options:

+ DFIXED_POTENTIAL: switches on the fixed potential
+ DNO_SELF_GRAVITY: removes all self gravity (it is still calculated, though, so this does not offer any considerable speedup -- this should be fixed in the future)
