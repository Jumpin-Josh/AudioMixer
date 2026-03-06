# AudioMixer
I've been interested in analog electronics and electronic instruments for a decent chunk of my time in college so I wanted to try my hand at creating an [audio mixer](https://youtu.be/q8tmUgaXrEQ?si=pKyhKzkajhBQ0o0y&t=1063) using a design I found online. This will be the first part of a bigger project where I hope to make a few different analog synthesizer modules and use the mixer to, well, mix them together. :)

### Audio Mixer Design
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Prototype.png "Initial Mixer Design in LTSpice")
All three of the 100k potentiometers is setup in a voltage divider configuration allowing each input to be attenuated independently. The inputs are then tied together and fed into two inverting amplifiers to boost the resulting signal since the input pots may reduce the amplitude. The 20k potentiometer is used to add/adjust clipping on the mixer's output which is then fed into another op-amp since the clipping reduces the signal amplitude yet again. (Each potentiometer can be swept through using a .step directive to see how different values will affect the waveform.)

Sidenote: using one non-inverting amp in place of the two inverting amps doesn't provide enough gain to the mixer's output.
