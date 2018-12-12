# doom2max
Audio and visuals from Doom2 (doomsday engine) into Max 8 via Soundflower/Jack (audio) and Syphoner (visuals). A hastily produced initial demo is [available](https://github.com/matdwlv/doom2max/blob/master/quick%20demo.mp4).

Audio signal flow is:

Doom2 (via doomsday engine) => Soundflower (or Jack) => Max (adc~)

Visual flow is:

Doom2 (via doomsday engine) => Syphoner => Max (jit.gl.syphonclient)

Within **doom2 AV.maxpat** (included in the project zip file), the visual part of the patch firstly tracks brightness in a small square around the centre of the screen. If the pistol (specifically the pistol, but may work for other guns too - untested) is fired, the brightness of the square reaches 250 (i.e. bright white), with the select object being used to trigger further audio and visual processing: essentially, firing the gun triggers a transition into two seconds of trippy, wobbly audiovisual disorientation via stereo variable delay line (audio) and video feedback+rotation (visual), the parameters of which are lightly randomised. 

Required software:

- [Max 8](https://cycling74.com/downloads) (the free demo will do)
- [Syphoner](http://www.sigmasix.ch/syphoner/)
- Doom2 (I've used the [Doomsday engine](http://dengine.net/) version, but others should work too)

If you're on Windows rather than Mac, you could try using [Sprout](http://spout.zeal.co/) or jit.desktop (from within Max) instead of Syphon/er (both are untested). Xsplit gamecaster is another possiblity (also untested).

