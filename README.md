# AudioMixer
I've been interested in analog electronics and electronic instruments for a decent chunk of my time in college so I wanted to try my hand at creating an [audio mixer](https://youtu.be/q8tmUgaXrEQ?si=oKsCojngbPTezQQb&t=1473) using a design I found online. This will be the first part of a bigger project where I hope to make a few different analog synthesizer modules and use the mixer to, well, mix them together. :)

### Table of Contents
1. [Initial Simulations](https://github.com/Jumpin-Josh/AudioMixer/blob/main/README.md#initial-simulations)
2. [Breadboard Prototyping](https://github.com/Jumpin-Josh/AudioMixer/blob/main/README.md#breadboard-prototyping)
3. [PCB Design and Circuit Assembly](https://github.com/Jumpin-Josh/AudioMixer/blob/main/README.md#pcb-design-and-circuit-assembly)
4. [Enclosure Design](https://github.com/Jumpin-Josh/AudioMixer/blob/main/README.md#enclosure-design)
5. [Final Product and Closing Thoughts](https://github.com/Jumpin-Josh/AudioMixer/blob/main/README.md#final-product-and-closing-thoughts)

## Initial Simulations
Cause who doesn't enjoy some circuit simulation? It's the LT*Spice* of life!
### Audio Mixer Design
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Circuit.png "Initial Mixer Design in LTSpice")
All three of the 100k potentiometers are setup like voltage dividers allowing each input to be attenuated independently. The inputs are tied together and fed into two inverting buffers<sup>1</sup> to boost the resulting signal since the input pots may reduce the amplitude. The 20k potentiometer is used to tune the clipping on the mixer's output which is then fed into a non-inverting buffer. The .step directive is used to sweep through multiple potentiometer values to see how it will affect the signal.

[1]: The first inverting buffer is used so that the input signals are summed rather than averaged. This is done so that if any of the inputs are at 0V it won't affect the other input signals. The second inverting buffer is used to negate the first inversion in case I want to mix in a control voltage (CV) from a low frequency oscillator (LFO) or envelope generator (I plan on building both in future).
### Signal Analysis
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%201.png "Input and output signals of the mixer")
Above are the input and output waveforms of the mixer with all input pots at max "volume".
#### Closer look at the output signal
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%202.png "Output signal")
Note the signal has some clipping as it reaches the supply voltages even though this is the raw output.
#### Effect of the clipping diodes
![alt text](https://github.com/Jumpin-Josh/AudioMixer/blob/main/simulations/Mixer%20Waveforms%203.png "Sweep of the cliping potentiometers")
Simulation of the signal with no, half, and full clipping.

## Breadboard Prototyping
## PCB Design and Circuit Assembly
## Enclosure Design
## Final Product and Closing Thoughts
