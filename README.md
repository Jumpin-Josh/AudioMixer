# AudioMixer
I've been interested in analog electronics and electronic instruments for a decent chunk of my time in college so I wanted to try my hand at creating an [audio mixer](https://youtu.be/q8tmUgaXrEQ?si=oKsCojngbPTezQQb&t=1473) using a design I found online. This will be the first part of a bigger project where I hope to make a few different analog synthesizer modules and use the mixer to, well, mix them together. :)

## Initial Simulations
Cause who doesn't enjoy some circuit simulation?
### Audio Mixer Design
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Circuit.png "Initial Mixer Design in LTSpice")
All three of the 100k potentiometers are setup in a voltage divider configuration allowing each input to be attenuated independently. The inputs are then tied together and fed into two inverting buffers to boost the resulting signal since the input pots may reduce the amplitude. The 20k potentiometer is used to add/adjust clipping on the mixer's output which is then fed into another op-amp since the clipping reduces the signal amplitude yet again. (Each potentiometer can be swept through using a .step directive to see how different values will affect the signal.)

Sidenote: The first inverting buffer is used so that the input signals are summed rather than averaged. The second inverting buffer is used to negate the first inversion in case I want to mix a control voltage from a LFO or 
### Signal Analysis
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%201.png "Input and output signals of the mixer")
These are the input and output waveforms of the mixer with all input pots at max value. Note that the output signal has some slight clipping even though the clipping stage was not used.
#### Closer look at the output signal
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%202.png "Output signal")
#### Effect of the clippnig diodes
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%204.png "Sweep of the cliping pot")
Simulation of the signal with no, half, and full clipping.
