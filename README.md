-> Introduction
I used LTspice to play with a small NMOS transistor circuit. There is a resistor (R1) and a power supply of 1.8V. The gate of the transistor gets a tiny AC signal from another source. This setup helped me look at the transistor’s DC operating point, how it behaves with different frequencies (AC analysis), its DC output, and its time response (transient).

![1](https://github.com/user-attachments/assets/f39ff6f7-9b2d-445c-b9b7-15dc25095e59)


-> Operating Point and Id Value
I did a DC operating point analysis to find important voltages and currents. The gate was around 0.9V, and the drain was about 1.77163V. Because the source is near ground, that means the transistor is in the saturation region and can act like an amplifier. The drain current turned out to be around 28.37µA.

->AC Analysis
Next, I checked the circuit’s frequency response using AC analysis. At lower frequencies, the circuit has a steady gain, but at higher frequencies, the gain gets weaker. The phase also changes as we move through different frequencies. This looks just like a simple low-pass amplifier using an NMOS transistor.

![ac1](https://github.com/user-attachments/assets/f6ac09e6-8e22-49f8-980e-f239468db099)


->DC Output Characteristics
Then I used a DC sweep to see how the circuit’s output changes with different voltages. I noticed that the drain voltage stayed around 1.77V, which matched what I expected from the resistor and transistor math. This tells me the transistor is getting the right bias and is working where it should.

![dc1](https://github.com/user-attachments/assets/989a2e5b-2b70-4861-b410-2c9df209371a)


-> Transient Analysis
I also tried a transient analysis to watch how the circuit behaves over time. I fed the gate a little sine wave and checked the voltage at the drain. The output was amplified, and at really high frequencies, it looked a bit distorted. That still shows the NMOS can amplify signals, and everything worked like I thought.

![Transient](https://github.com/user-attachments/assets/9b6f6cc8-672f-4024-9c25-7f82db4ea464)


-> Conclusion
After doing all these tests—DC operating point, AC sweep, DC sweep, and transient—I saw that the NMOS transistor is well biased and works as an amplifier. 
