##### ***Remeber***:

> We need to distinguish between:
> 1. **Low frequency signals** or DC signals.<br>So If the quantity we are measuring changes its values really slowly.
> 2. **High frequency signals**.

---

> For **low frequency signals**, we will need an **AC exitation** to make the capacitive sensor work.
> Since the signal $g(t)$ varies slowly, what happens is that the capacitance takes a value which is constant for a long time.<br>This time is enough to allow the **loss of the charge** which is stored in the capacitors due to the parasitic resistances.<br>==Remember that when thinking to a capacitance, we also have to imagine that there is always this parallel resistance: $R_F$==.<br>⇒ In this case we need to vary the charge by exciting the capacitance with **AC excitations** (so a variable excitation), so $V_C$ will be an AC exitation (for simplicity a sine wave).<br>==Also the frequency of the excitation ($f_{exc}$) has to be selected, and it has to be much larger than the maximum signal frequency ($f_{S_{MAX}}$)==.
> 
> We have found two different readout solutions to the low frequency signal problem:
> 1. [[SaM - FM (Frequency Modulation) Based on Oscillators|FM: Frequency Modulation]] which uses a **grounded sensor**.
> 2. [[SaM - Complete AM (Amplitude Modulation) Circuit|AM: Amplitude Modulation]] which uses an **unreferenced sensor**.

---

So, we spoke about [[SaM - Types of Capacitive Sensors|capacitive sensors]] and about [[SaM - Electrical Noise|the main problem of capacitive sensors]]:
- We underlined that there is the need of using [[SaM - Shields|shields]].
- We also underlined the [[SaM - Differences Between Grounded and Un-grounded Capacitive Sensors|difference between grounded sensors and unreferenced capacitive sensors]] because they admit different solutions, for the **read-out electronics**.

So now we will say something more about the readout electronics for capacitive sensors.
We distinguish two different applications for these sensors, the first is related to low frequency signal and it is the first one that we will discuss.
![[Pasted image 20230719105116.png]]

First of all, we'll speak about the case in which capacitive sensors are used to measure
low signals or static signals.
![[Pasted image 20230719105125.png]]
- So the quantity $g$ that it is sensed by the sensor is a slow varying signal, this signal here is referred as $g(t)$ so the **input of the sensor**.
- We will have a sensor which transduces this quantity into the capacitance.<br>So our sensor will give us $e(t) = C(g(t))$, where:
	- $e$ : output of our sensor
	- $C$ : means that the output will be a capacitance depending on $g$
	- $g$ : input of the sensor
- So in any case this signal here varies slowly, and what happens is that the capacitance takes a value which is constant for a long time.<br>This time is enough to allow the **loss of the charge** which is stored in the capacitors due to the parasitic resistances.<br>==Remember that when thinking to a capacitance, we also have to imagine that there is always this parallel resistance: $R_F$==.<br>⇒ In this case we need to vary the charge by exciting the capacitance with **AC excitations** (so a variable excitation), so $V_C$ will be an AC exitation (for simplicity a sine wave).<br>Also the frequency of the excitation ($f_{exc}$) has to be selected, and it has to be much larger than the maximum signal frequency ($f_{S_{MAX}}$).
- Remember that for capacitive sensors, we have to distinguish always between:
  1. **Grounded sensor**, (remember about proximity sensors).<br>So this kind of sensor which has the requirement of having one of the two terminals referenced.
  2. And the other type are a **referenced sensors**.<br>In this case we are completely free to choose the best readout topology, because we have no constraints about the grounding of one of the two terminals.

Under all these assumption we can find two types of readout electronics:
![[Pasted image 20230719105134.png]]
- **FM modulated**:<br>Circuits which are based on a strategy which considers the frequency modulation of the signal.
- **AM modulated**:<br>Based on amplitude modulation.
