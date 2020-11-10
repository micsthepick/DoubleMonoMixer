# DoubleMonoMixer

Takes two mono signals, and mixes them using the hilbert transform so that they are out of phase
but present in both channels, so that they can also be unmixed

 ## Usage
copy to the usual location to store JSFX. (usually %appdata%/REAPER/EFFECTS for reaper)
Will also need to grab a zip version of [cookdsp](https://github.com/belangeo/cookdsp) and unzip that to the same location
Put two mono signals in the same stereo track, and apply the effect.
Whether you enable "encode" or "decode" first does not matter, as long as you do the opposite, then
things should return to their orignial phase (should, innacuracies expected due to the accuracy of the hilbert).
If one track is mono, then the result will have the same signal in both tracks, but 90 degrees out of phase,
which when combined with vocalrediso.jsfx, can be isolated with phase2 = -90 for "encode" and phase2 = 90 for "decode" if you have just one track in L, and silence in R.