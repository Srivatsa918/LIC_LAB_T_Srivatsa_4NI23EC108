EXPERIMENT 3:-

Q]Design and analyze the differential amplifies for the following specificahon VDD=1.8V, P≤ 2.2 mW, Vicm = 0.95V, Vocm = 1.1V, Vp=0.4V. perform: DC analysis, Transient analysis, Frequency responce and extract the parameters.



1] Introduction:-
A differential amplifier is one of the elementary blocks utilized in analog circuit design, used widely for amplification of high common-mode rejection signals. It amplifies the differential input and rejects common noise, one of the most important applications in sensor signal processing, communications systems, and operational amplifier circuits. The circuit is usually made up of two transistors or MOSFETs with common source/emitter resistance for balanced operation. The DC operating point, transient response, and AC analysis of a MOSFET differential amplifier simulated with LTSpice are presented in this report.


Requried Caluclations:-



Circuit_1:-
![1](https://github.com/user-attachments/assets/47e2b2bc-9492-4a23-a7bb-49df2d225f6f)

2] DC Operating Point Analysis:-


![2](https://github.com/user-attachments/assets/f2f0bfce-46d2-457a-98c1-572401f36872)


3] Transient Response:-
Transient analysis monitors the time-domain response of the circuit to the input signal. A 0.95V amplitude sine wave input with 0.1V AC component of 1kHz frequency was applied. The output waveform monitors the differential response of the circuit, showing how the amplifier responds to dynamic signals. The MOSFETs are in the active region, enabling proper amplification. The results confirm the expected differential operation, with the output swinging symmetrically around the bias point as a response to the input signal changes.

![3](https://github.com/user-attachments/assets/e522b664-c9ba-4b00-a897-9bd8f2df6d43)


4] AC Analysis:-
The AC analysis sets the frequency presponse of the amplifier with a small-signal AC input and measurement of the gain and phase shift over a large range of frequencies. The simulation was set with the .ac dec 20 0.1 1T command, sweeping the frequency logarihmically between 0.1 Hz and 1 THz in 20 points per decade. This determines the gainbandmwidth product, midband gain, and high-frequency rolloff. The amplifier indicates high gain for low and mid-frequencies and a smooth roll-off at high freuencies due to parasitic capacitances and MOSFET operation. The bandwidth and phase response determine the suitablity of the design for differential signal amplification in real-world applications.

![4](https://github.com/user-attachments/assets/2dbdaf99-9086-4545-a5ed-af9edc9f83e5)








Q]Circuit_2
![1](https://github.com/user-attachments/assets/ddf1de92-190a-4dea-a285-c85b55f925fd)


1] DC Operating Point Analysis:
The given circuit is a CMOS differential amplifier with NMOS tranistors (M1 and M2) in differential pair. The circuit is supplied with a power supply voltage (VDD) of 1.8V, and both input terminals are biased to 0.95V (Vicm1 and Vicm2). The load resistors (RD1 and RD2) are each 1.145kΩ, and the current source (ISS) provides 1.222mA, which provides equal current division to M1 and M2.

- V(n003) and V(n002) (Drain Voltages) ≈ 1.1004V
- V(n005) (M1 and M2 Source Voltage) ≈ 0.400017V
- V(n006) and V(n004) (Gate Voltages) = 0.95V 
- V(n001) (VDD = 1.8V

- Currents:
- M1 and M2 drain current (Id(M1) & Id(M2))* ≈ 611µA (0.000611A)
- M1 and M2 source current (Is) ≈ 0.000611A
- Via RD1 and RD2 ≈ 611µA
- ISS current supplied ≈ 1.222mA

- ![2](https://github.com/user-attachments/assets/009e3d08-210f-43a8-909f-ac413f553973)


These readings confirm that the circuit is well-biased, with the trsistors in the saturation region as would be the case for a differential amplifier.

2]Transient Analysis:
The transient response waveform shows the differential output voltage varying sinusoidally with time. This shows that the circuit is performing as expected to an input signal and producing the expected amplification. The input signals are small AC fluctuations on the *common-mode DC voltage of 0.95V.
- The result demonstrates a clean sinusoidal response with correct differential operation.
- Waveform phase and amplitude show that the circuit is where it is expected to be, in its linear region.

![3](https://github.com/user-attachments/assets/02a004a2-3073-4960-8b64-4bb1b1c723a1)

This analysis verifies that the differential amplifier operates as expected under dynamic conditions to enable efficient signal amplification.

3] AC Analysis:

AC frequency response plot illustrates the differential amplifier gain across a wide frequency range. The response is flat at low frequencies with a fairly flat gainin the mid-band. But at high frequencies, the gain starts to decline, and this is the bandwidth limitatin of the amplifier.

![4](https://github.com/user-attachments/assets/9125ee0f-c3c3-4680-be80-98baacbdaf1f)







Q]Circuit_3:-
![1](https://github.com/user-attachments/assets/fe7d5d8e-14c0-42bb-ad1f-721860316c28)


1]DC Operating Point Analysis:-
The differential amplifier, built with NMOS transistors and a current source, operates symmetrically with input common-mode voltages of 0.95V at nodes n006 and n004. Drain voltages at  M1  and  M2  are 1.1004V, while the source voltage is 0.400017V. Bias voltage Vb is 0.76V, properly biasing M3. Drain currents through RD1 and RD2 are 611 µA, matching M1 and M2. The total supply current is 1.222 mA, confirming proper current mirroring. Negligible gate currents indicate ideal MOSFET behavior.  

![2](https://github.com/user-attachments/assets/af9bf103-97e5-4c27-96e8-5c46f10deb3f)


2]Transient Analysis:-  
Over a 5 ms span, the transient response shows proper differential signal amplification with maintained phase relationships. The output waveform exhibits expected peaks and troughs, ensuring transistors operate within their designed regions without saturation or cutoff. 

![3](https://github.com/user-attachments/assets/09fee891-afca-4957-9315-fb43f2be60ac)


3]AC Analysis:-
The gain plot remains stable in the mid-frequency range before rolling off at high frequencies due to the circuit's dominant pole. The phase response initially holds steady before decreasing with frequency. The results confirm the amplifier's effective signal amplification within its designed bandwidth.  

![4](https://github.com/user-attachments/assets/8ac9f122-c6c6-4d0d-913f-aef6ad474954)



=>Conclusion:-  
The circuit simulation results indicate that the designed NMOS-based amplifier operates within expected parameters. The key voltage levels at various nodes confirm proper biasing, while the current values validate the correct functioning of the active components. The AC analysis shows stable frequency response, and the transient response suggests smooth signal amplification.  

=>Inference:-
1. Voltage Levels: The circuit maintains appropriate voltage levels across different nodes, ensuring reliable operation.  
2. Current Flow: The drain and source currents align with theoretical expectations, confirming proper transistor biasing.  
3. Frequency Response: The AC analysis shows a well-defined bandwidth, making the circuit suitable for the intended application.  
4. Performance Stability: The transient response data indicates minimal distortion, suggesting good amplification characteristics.  
