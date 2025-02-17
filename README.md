EXPIREMENT-1

-> Introduction
I used LTspice with a small NMOS transistor circuit. There is a resistor (R1) and a power supply of 1.8V. The gate of the transistor gets a tiny AC signal from another source. This setup helped me look at the transistor’s DC operating point, how it behaves with different frequencies (AC analysis), its DC output, and its time response (transient).

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
![Screenshot 2025-02-17 234456](https://github.com/user-attachments/assets/a4784ad0-a9c2-45f8-b076-9bc4a610d3c8)



-> Conclusion
After doing all these tests—DC operating point, AC sweep, DC sweep, and transient—I saw that the NMOS transistor is well biased and works as an amplifier. 






Design-2

![Screenshot 2025-02-18 002528](https://github.com/user-attachments/assets/37d195d5-1376-46fb-9116-d4fd5b8d4fcc)



-> Introduction
The report below is an overview of the outcome of circuit simulation from a SPICE-based simulator, e.g., DC operating point analysis, transient analysis, AC analysis. The circuit uses PMOS (CMOSP) and NMOS (CMOSN) transistors, which influence the switching behavior. A 50mV amplitude, 1kHz frequency sine wave voltage source is applied.

![Screenshot 2025-02-18 002547](https://github.com/user-attachments/assets/fa8b68cc-727e-4d1c-a870-bce63159cf41)
![Screenshot 2025-02-18 002600](https://github.com/user-attachments/assets/1219d06e-ddac-4e90-83f3-b25b9134ebd9)
![Screenshot 2025-02-18 002612](https://github.com/user-attachments/assets/536d4194-5ed2-469c-992f-7001f93d833a)





-> AC Analysis
The AC analysis gives the frequency response, gain, and bandwidth of the circuit. For sweeping frequency from 0.1Hz to 1Hz on a log scale, the .ac dec 20 0.1 1 respectively was used. This analysis is useful in determining the response of the circuit to different frequencies, gain characteristics, and possible signal attenuation.

![Screenshot 2025-02-18 002726](https://github.com/user-attachments/assets/c8757302-6ca7-41d8-9c2d-ac717ff5beee)


-> DC Operating Point Analysis
A DC sweep was conducted by sweeping vin from 0V to 1.8V in 0.1V steps using the .dc vin 0 1.8 0.1 command. This analysis gives voltage transfer characteristics, showing the operating regions of transistors and helping in setting biasing conditions. The results show the circuit under steady state conditions and help in design implementation.

![Screenshot 2025-02-18 002627](https://github.com/user-attachments/assets/1753918a-dc32-442c-b776-32aa094e2901)


-> Transient Analysis
The transient response was analyzed using the .tran 1m command to check the dynamic behave of the circuit over time. This is useful in checking rise time, fall time, and signal propagation characteristics. Observations include possible instability in the switching behavior, which is imprtant in ensuring reliable circuit operation.

![Screenshot 2025-02-18 002904](https://github.com/user-attachments/assets/1d322d87-8c77-4a11-9434-ae1ae0df62f4)


-> Conclusion
Simulation output provides valuable information regarding the voltage transfer function of the circuit, signal response, and frequency response. MOSFET sizes need to be checked to ensure optimal performance, transient response should be checked for instability, noise analysis should be performe, and the biasing conditions should be set to gey stability and efficiency. The results are used to build a better quality design of circuit.
