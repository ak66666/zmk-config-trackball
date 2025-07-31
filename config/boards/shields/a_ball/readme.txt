20250730 1442

The layer-based direction switch works now.
My mistake was to put &zip_xy_swap_mapper and some other transformations into the base/default layer 0.
It was not turning off, or didn't play well with a similar transformations in other layers.
Once I removed everything from layer 0  (the default left hand configuration), and put the XY swap 
into layer 1 (the right hand layout), and set all the defatul XY swap and X- and Y-inversions in the config file,
that functionality started working.

The scrolling works for the left-hand configuration only.
I suspect that's because of the way I switch between the layers - and it never goes to the level 3 (right hand scrolling.)
I will remove that separate right hand scrolling layer, and leave a single scrolling layer.
The XY swap will be done in layer 2 for both scrolling and pointing.

20250730 1911

Started laying out the keys.
I have 9 pins available for direct control - on the left side of PriMicro, 1..9.
That leaves 0 for the ball irq and two ground pins.

I seem to be unable to move to a layer after the next one - in the trackball listener code.
It is simply ignored, even the laye is selected - I confirmed it by placind specific letter on those layers.
 
