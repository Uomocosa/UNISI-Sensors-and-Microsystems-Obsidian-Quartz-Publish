# Index
- [[#Applications for Capacitive Sensors (FM & AM Oscillators)]]
- [[#FM Modulation Based on Oscillators]]
- [[#AM Modulation Based on Oscillators]]

---
##### Applications for Capacitive Sensors (FM & AM Oscillators)
So, we spoke about capacitive sensors and about the main problem of capacitive sensors:
- We underlined that there is the need of using **shields**.
- We also underlined the difference between rounded sensors and unreferenced sensors because they admit different solutions, for the readout electronics

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
- **FM modulated**:<br>So these are circuits which are based on a strategy which considers the frequency modulation of the signal.
- **AM modulated**:<br>We will understand immediately what it means.

---
##### FM Modulation Based on Oscillators
***FM : Frequency Modulation***
![[Pasted image 20230719105145.png]]
- This type of circuit are based on oscillators.
- So I take an example, which is a special oscillator called **relaxation oscillator**, which actually is a **square wave oscillator**.
- The AO in this case works as a **comparator**.
- In this circuit the **time** (or **period**) it takes for the output to switch from $+V_{0_{MAX}}$ to $-V_{0_{MAX}}$ is a function of the sensor's capacitance $C_S$.

So to get the sensor value we need to:
![[Pasted image 20230719105154.png]]
- So our sensitivity and offset are both equal to: $\frac{\alpha}{C_0}$
- Where:
	- $\frac{\alpha}{C_0} = \frac{1}{2RC_0\ln{\left(\frac{1-\beta}{1+\beta}\right)}}$
	- $\beta = \frac{R_1}{R_1+R_2}$
	- Also we previously have defined $C$ as $C= \frac{C_0}{1+x}$, where $x$ is the varying part, as it is the sensor's capacitance it can change.
- Also more in general we can say that **the Frequency of an FM Modulation** can be defiened as:$$f(t) = f_0\left(1+\frac{f_A}{f_0}x(t)\right)$$
- $f(t)$ represents a **fequency** (it was defined as the inverse of the period $T$)

> **NOTE**:
> In the notes there is a **WRONG** simplification:$$\frac{1}{\ln\left(\frac{1+\beta}{1-\beta}\right)} \neq \ln\left(\frac{1-\beta}{1+\beta}\right)$$
> As you can see this is wrong, (if it was right the real part, in blue, should be all equal to $0$, and there should not be an imaginary part):<br>![[Pasted image 20230920144248.png]]

So in general referring to the sine wave, we have an output which is this one:
![[Pasted image 20230719105202.png]]
- $x(t)$: our **target signal** (what we want to measure).
- We can have a phase $\varphi$ if we want to, but it's not so important.
- The frequency and the phase are variable with time.
- ==*If for instance if I have $x(t)$ which is a slow invariant signal, then the frequency would start at a low value and then increase and increase and increase*==.
- The requirement of having $f_0 \gg f_{S_{MAX}}$, indicates that this variation here is much slower than the variation of the basic signal, it is like the excitation signal is complex.
- ***Why the Integral?***:
	- The reason is purly mathematical, but to understand let's make an example:<br>*Suppose the signal does not vary, so the voltage should be somenthing like:*$$V_o(t) = V_0 \kern2px sin(2\pi t)$$*Tho it may vary.<br>If it does, we need to account for each little, infinitesimal, variation, to do so we need an integral*. 


So this is a frequency modulated signal and we know that the bandwidth that we obtain is infinite, but if the maximum frequency of the signal ($f_{S_{MAX}}$) is much smaller than the base frequency ($f_0$) then we can approximate in this way the bandwidth of the **FM signal** which is:<br>![[Pasted image 20230719105215.png]]

- Where: 
	- $\Delta f_{MAX} = f_A \cdot x_{MAX}$.
	- And $f_A$ comes from: $f(t) = f_0\left(1+\frac{f_A}{f_0}x(t)\right)$
- The complete FM circuit has this topology here: ...
- We can say that this kind of readout electronics, since it transforms a variation of the input quantity into a variation of frequency is a very robust solution to **reject noise**.
- ***What do we mean with bandwith of a signal?***
	- The bandwidth of a signal refers to the range of frequencies contained within that signal.<br>In the context of signals, such as audio or electromagnetic waves, it represents the difference between the highest and lowest frequencies present in the signal.
	- Mathematically, the bandwidth (\(B\)) is often defined as:
	- $B = f_{\text{high}} - f_{\text{low}}$
	- Where:
		- $B$ is the bandwidth.
		- $f_{\text{high}}$ is the highest frequency component in the signal.
		- $f_{\text{low}}$ is the lowest frequency component in the signal.
	- For example, in the case of an audio signal, if the lowest frequency is $20$ **Hz** and the highest frequency is $20,000$ **Hz** (or $20$ **kHz**), then the bandwidth of that audio signal is $20,000 \, \text{Hz} - 20 \, \text{Hz} = 19,980 \, \text{Hz}$.
	- Understanding the bandwidth of a signal is important in various fields, including telecommunications, signal processing, and electronics, as it determines how much information the signal can carry and how it can be transmitted or processed efficiently.

The complete FM circuit has this topology here:
![[Pasted image 20230719105215 - Copia.png]]
- The sensor which is part of the oscillator, as we have seen previously.
- $f_{\Delta x}(t)$ is the function that previosly we defined as ${f_A}\cdot x(t)$
- Note that $V_0'$ has no "frequency offest" $f_0$, it was removed thanks to the signal $V_R$.
- The **FM Demodulator** has the job of giving as output a\kern2px  voltage related to the frequency in input.
- This kind of solution is used for signals which can be static but also they have a large bandwidth up to $100 \kern2px kHz$.
- the typical value for $f_0$  is $2 \kern2px MHz$ (much larger than the maximum signal frequency).

---
##### AM Modulation Based on Oscillators
***AM: Amplitude Modulation***
![[Pasted image 20230719105223.png]]
- This time we define $C = C_0 \cdot (1+x)$, and it has to be an **unreferenced sensor**.
- $C_R$: reference capacitance
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

---
##### Summary of AM and AF Modulated Circuits
We have seen **AM modulated circuits**, **FM modulating circuits**.

Then we have seen two special types of **readout front end circuit**, which is the **direct digital capacitive conversion** and the **switching capacitor circuit**, these can be used for static signals, also for signals which are **slowly varying**.

Then some of these is more suitable to be used also for signals which have large bandwidth and other instead for really slowly varying signals.
But in any case, they can be in principle used also for static signals.

---