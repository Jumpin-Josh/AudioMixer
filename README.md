# AudioMixer + Kick Drum Circuits
I've been interested in analog electronics and electronic instruments for a decent chunk of my time in college so I wanted to try my hand at creating an audio mixer using a design I found [online](https://youtu.be/q8tmUgaXrEQ?si=pKyhKzkajhBQ0o0y&t=1063). This will be the first part of a bigger project where I hope to make a few different analog synthesizer modules and use this mixer to, well, mix them together. :)

### LTSpice Prototype Simulation
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Circuit.png "LTSpice Simulation")
Each of the 100k potentiometers is setup in a voltage divider configuration allowing each input to be attenuated. The inputs are then tied together and fed into two inverting amplifiers to boost the resulting signal since the input pots may reduce the amplitude. The 20k potentiometer is used to add/adjust clipping on the mixer's output then fed into another op-amp since the clipping reduces the signal amplitude yet again.
