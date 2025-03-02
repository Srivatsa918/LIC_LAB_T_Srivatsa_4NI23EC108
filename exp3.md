1] Introduction:-
A differential amplifier is one of the elementary blocks utilized in analog circuit design, used widely for amplification of high common-mode rejection signals. It amplifies the differential input and rejects common noise, one of the most important applications in sensor signal processing, communications systems, and operational amplifier circuits. The circuit is usually made up of two transistors or MOSFETs with common source/emitter resistance for balanced operation. The DC operating point, transient response, and AC analysis of a MOSFET differential amplifier simulated with LTSpice are presented in this report.


![1](https://github.com/user-attachments/assets/47e2b2bc-9492-4a23-a7bb-49df2d225f6f)

2] DC Operating Point Analysis:-
The DC operating point determines the voltages and currents in the circuit without an input signal applied. The resulting values are important in determining whether the MOSFETs are in the desired operating region. From the LTSpice simulation, the most significant node voltages and currents are the following: The drain voltage across M1 is 95V, and that across M2 is -95V. The source voltage for both transistors is at -100.38V, and the gate voltage is -8V. The drain current through M1 is 0.000611026 A, and the source current is the same but in opposite direction, for current conservation. Similarly, the bias current through the RD1 resistor is 0.00122205 A, indicating balanced differential operation. The introduction of a common-source resistor compromises the symmetry and stability of the circuit.

![2](https://github.com/user-attachments/assets/f2f0bfce-46d2-457a-98c1-572401f36872)


3] Transient Response:-
Transient analysis monitors the time-domain response of the circuit to the input signal. A 0.95V amplitude sine wave input with 0.1V AC component of 1kHz frequency was applied. The output waveform monitors the differential response of the circuit, showing how the amplifier responds to dynamic signals. The MOSFETs are in the active region, enabling proper amplification. The results confirm the expected differential operation, with the output swinging symmetrically around the bias point as a response to the input signal changes.

![3](https://github.com/user-attachments/assets/e522b664-c9ba-4b00-a897-9bd8f2df6d43)


AC Analysis-
The AC analysis sets the frequency presponse of the amplifier with a small-signal AC input and measurement of the gain and phase shift over a large range of frequencies. The simulation was set with the .ac dec 20 0.1 1T command, sweeping the frequency logarihmically between 0.1 Hz and 1 THz in 20 points per decade. This determines the gainbandmwidth product, midband gain, and high-frequency rolloff. The amplifier indicates high gain for low and mid-frequencies and a smooth roll-off at high freuencies due to parasitic capacitances and MOSFET operation. The bandwidth and phase response determine the suitablity of the design for differential signal amplification in real-world applications.

![4](https://github.com/user-attachments/assets/2dbdaf99-9086-4545-a5ed-af9edc9f83e5)




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

