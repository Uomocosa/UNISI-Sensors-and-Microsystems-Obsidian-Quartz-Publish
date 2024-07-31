##### ***Remeber***:

> The simplest circuit for Amplitude Modulation:<br>![[Pasted image 20230719105223 1.png|500]]
> The output will be:$$V_o(t) = \frac{C_0}{C_R}(1+x) \cdot V_g$$Where: $V_g = V \sin(2\pi f_0 \kern2px t + \varphi)$

> We have defined the general formula of the AM modulation as:$$V_0(t) = V_R\kern2px[1+mx(t)] \sin(2\pi f_0 \kern2px t + \varphi)$$Where:
> - $V_R = V\cdot {C_0 \over C_R}$
> - $m$ is a **modulation factor** and we have that $|m|\approx 1$ (usally less than $1$).

> From the spectrum we understand that if this frequency $f_0$ is much larger than the value of the maximum frequency of the signal $f_{S_{MAX}}$, then the recover of the signal is easier:<br>![[Pasted image 20230719105232 1.png|500]]
> Instead, if the shifted frequency were more close to the original frequency (the base band) of the signal, then there will be difficulties in the demodulation process.
> 
> We have also seen the [[SaM - Complete AM (Amplitude Modulation) Circuit|complete circuit for amplitude modulation]]. #IMPORTANTE 

> We can list a certain amount of circuits, which are good for this application:<br>![[Pasted image 20230719105246.png]]
> - **[[SaM - Current Amplifier|Current]] or [[SaM - Charge Amplifier|charge amplifiers]]**.<br>And this obviously can be used with ==unreferenced signals and sensors==.
> - **AC [[SaM - Resistive Bridge • Wheatstone|bridges]]**.<br>Like we have seen the resistance bridges, we can form bridges with capacitance and resistances.<br>==This is good for both referenced sensors and grounded ones==.
> - **Voltage dividers**:<br>==Which can be used with unreferenced and grounded ones==.

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_5.jpg]]

---
***AM: Amplitude Modulation***
![[Pasted image 20230719105223.png]]
- This time we define $C = C_0 \cdot (1+x)$, and it has to be an **unreferenced sensor**.
- $C_R$: reference capacitance.
- $V_g$ and $R_g$ : AC source and resistance.<br>$R_g$ is considered to be very small so I will neglect it from now on.<br>In practice this means that we have to take a good voltage generator.
- And we have seen that this is a good solution because, in terms of sensitivity to **electrical noise**.
- $f_0$ is the excitation frequency, so I select it arbitrarily.
- The output function is a little wrong: $$V_o(t) = \frac{C_0}{C_R}(1+x) \cdot V \sin(2\pi f_0 t + \varphi)$$
![[Pasted image 20230719105232.png]]
- $V_R = V \cdot \frac{C_0}{C_R}$
- So in general, using solutions like this in which our capacitance is a part of the gain of the circuit (of the amplifier) with a topology selected in the particular case to be suitable for this situation.
- $|m|$ is usually less than 1, like before (in the **FM** we called it $f_A$ to enfasize that in **FM** we talk about **frequency**, in **AM** about **amplitude**, they should both represent the sensitivity of the capacitive sensor #NOT_SURE_ABOUT_THIS ).
- Here the bandwidth is easily found, so the description of the signal in the frequency domain is easily found.
- If this was the spectrum of the signal base band, the original spectrum, then the modulated signal is this one, and it's frequency shifted, obviously by the modulation process.<br>From the spectrum we understand that if this frequency $f_0$ is much larger than the value of the maximum frequency of the signal $f_{S_{MAX}}$, then the recover of the signal is easier.<br>Instead, if this is more close to the frequency of the signal, then there will be difficulties in the demodulation process.

And so we can list a certain amount of circuits, which are good for this application:
![[Pasted image 20230719105246.png]]
- **Current** or **Charge Amplifier**.<br>And this obviously can be used with ==unreferenced signals and sensors==.
- **AC Bridges**.<br>Like we have seen the resistance bridges, we can form bridges with capacitance and resistances.<br>==This is good for both referenced sensors and grounded ones==.
- **Voltage Divider**:<br>==Which can be used with unreferenced and grounded ones==.

So for the complete **AM** circuit, I'll do two examples, one for **differential capacitance sensors**:
![[Pasted image 20230719105246 - Copia.png]]
- Note: this is an **inverting amplifier**.
- So differential because the capacitances are:
	- $C_1 = \frac{C_0}{1+x}$
	- $C_2 = \frac{C_0}{1-x}$
- $R_f$ : needed to reduce the effects of DC errors of the amplifier.
- And then we can perform a **synchronous AM demodulation** (for instance, a charge amplifier), then low pass filter, and finally the output.

[Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKACcQ09OUAWThIR78qYeOwFCwGIdmxSZUZHBYBDSZ15U5QvlW5gkTJGPhwQDGGa3YZkBGD4Zeg3hiSizkFgHcNKPg1pIW8-HU1teXBFUJBwvRBeXm4E7BYAc39BDVwRKBYAN3BHYWKUcCSlCC1qKjroBAyy0uZylGy632ipSuDSlC6+sF7FPCoBgGNE5JAxxOIhOfqzYdI19Y3iC15YW0ItPEJCbBQTtyhYSFYppJSa3gWIpStrTbfSIR3IPcowbARMPZeNgLnBWH4Hrp7o9hiIupDZlQEbD8upBKJCFRCNkwJjZuAjIZlGYLC84C4rvY+HhiAgHt8XFUvCwpuiQI9sUJHst4BAGDtfpAyJQ4DhiCCXqwOGz9iBOXK8qZYjL+GzuV15bL5eq-GyUWqQhqcXjtYa-PLcVQMGhwHiBhCYZU9ZV7d1+vhSt5MnrFGyAnlYrdEXEonM0mFQ6JRp0ONaMVabQlPCpMnGnmnMOVOn5WhV+ENKrFc7xcW6S4bUzaHOU03SAxI08Ca1WSsnYuF-uU+p38hCZj2OwC4k02UHR9ze2XHlx5mbZ4lS6PS675U2QI2TpwjZ9N-L5NxlXjyxQ8fvJ3uonvCAeumzwnfr-lpafL9lwm2WSftI+rwfQbzSUuOBiD+NxhjGf45EcLZJTUL9El3bI1wMQkTC8KgGGIaBQMIU4XGtYg8AQYjGDEJkzHhR4ewRY9A0eat51oz8xxKBEGJ5eB3neRJdjsatBAQECIFgm5+yHBEew44CuM2bZeOvBA8HccVeEfWCc0UY9uyHV0+i0zTpyaYsYRKAE-28IpjKkVjS1ERJaGeC5GkydohDMjQEBiSd71YmYGPDEM3JKcIg1iVz53C0K4PC-yogYlCLCJJV4EA6xvj4xw3BcfY-2S7wOEi-solC4kJBnBFIonJUWCAA) :<br>![[Pasted image 20231202114753.png]]
