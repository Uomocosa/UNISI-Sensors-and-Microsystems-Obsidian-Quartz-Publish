##### ***Remeber***:

> We can use a [[SaM - Square Wave Oscillator|square wave oscillator]] with a capacitcance sensor insted of the simple capacapitance, doing this the periods of the square wave will be different, and by measuring them we will be able to calculate the value of the capacitance:<br>![[Pasted image 20230719105145.png]]
> - The formula that relates the period of the square wave to the capacitance is: (*NOT IMPORTANT*)$$T = 2RC \cdot \ln\left(\frac{1+\beta}{1-\beta}\right)$$Where $\beta$ is as always defined as: #IMPORTANTE $$\beta = \frac{R_1}{R_1+R_2}$$

> In general we can say that **the frequency** $f(t)$ of an FM modulation can be defiened as: #IMPORTANTE $$f(t) = f_0\left(1+\frac{f_A}{f_0}x(t)\right)$$Where:
> - $f_0$ is the frequency of the AC exitation.
> - $f_A$ can be seen as an "**accuracy**" that transforms the measured signal $x(t)$ into a frequency ($f_A \cdot x(t)$)
> - Another way to rewrite this formula could be: $f(t) = f_0 + f_A \kern2px x(t)$.

> Another way to perform Frequency Modulation is to use and integerator, and a sine wave exitation:<br>![[Pasted image 20230719105202.png]]
> - ==*For instance if I have $x(t)$ which is a slowly growing invariant signal, then the frequency would start at a low value and then increase and increase*==.<br>$f_{S_{MAX}}$ is the maximum frequency at which $x(t)$ varies, we have supposed it to be really low.
> - The requirement of having $f_0 \gg f_{S_{MAX}}$ indicates that the variation of the sine wave source, is much faster than the variation of the measued signal $x(t)$.
> - ***Why the Integral?***: #NOT_SURE_ABOUT_THIS 
> 	- The reason is purly mathematical, but to understand let's make an example:<br>_Ideally the measured signal will not not vary, so $\left[x(t) = x_0\right]$, giving us the "ideal" output voltage_:$$V_o(t) = V_0 \cdot \kern2px \sin\left(2\pi \kern1px(f_0+f_A\kern2px x_0)\cdot t\right)$$_However the signal $x(t)$ can vary, even if very slowly_.<br>_If it does, we need to account for each little, infinitesimal, variation, to do so we need an integral_.

> Since we know that the maximum frequency of the signal ($f_{S_{MAX}}$) is much smaller than the base frequency ($f_0$), as per hypothesis, then we can approximate in this way the bandwidth of the **FM signal**:<br>![[Pasted image 20230719105215.png]]
> - $\Delta f_{MAX} = f_A \cdot x_{MAX}$.
> - And $f_A$ comes from: $f(t) = f_0+f_A \kern2px x(t)$.
> - We can say that this kind of readout electronics, since it transforms a variation of the input quantity into a variation of frequency, **so it is a very robust solution to reject noise**.
> - ***Why is FM Modulation a Very Robust Solution to Reject Noise?*** (*ChatGPT*)
> 	- **Wide Frequency Band:** FM signals typically occupy a wider frequency band compared to AM signals.<br>This allows FM signals to use more of the available frequency spectrum, providing better noise rejection.

> We have also seen the ***Complete FM Circuit***:<br>![[Pasted image 20230719105215 - Copia 1.png]]
> - ==The sensor is part of the oscillator==, like we have seen for the **Schmitt Trigger**.
> - $f_0$ is the exitation frequency, and in this stage we shift the signal $V_0$ by $f_0$, bringing $V_0$ to the **base band**. ("we remove the $f_0$ frequency-offset")
> - The **FM Demodulator** has the job of giving as output a voltage related to the frequency in input.
> - ==This kind of solution is used for signals which can be static but also they have a large bandwidth up to $100 \kern2px kHz$==. #IMPORTANTE 
> - ==The typical value for $f_0$ is $2 \kern2px MHz$ (much larger than the maximum signal frequency)==. #IMPORTANTE 

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_4 1.jpg]]

---
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

---

So in general referring to the sine wave, we have an output which is this one:
![[Pasted image 20230719105202.png]]
- $x(t)$: our **target signal** (what we want to measure).
- We can have a phase $\varphi$ if we want to, but it's not so important.
- The frequency and the phase are variable with time.
- ==*If for instance if I have $x(t)$ which is a slow invariant signal, then the frequency would start at a low value and then increase and increase and increase*==.
- The requirement of having $f_0 \gg f_{S_{MAX}}$, indicates that this variation here is much slower than the variation of the basic signal, it is like the excitation signal is complex.
- ***Why the Integral?***:
	- The reason is purly mathematical, but to understand let's make an example:<br>*Suppose the measured signal does not vary $\left[x(t) = x_0\right]$, so the output voltage should be somenthing like:*$$V_o(t) = V_0 \cdot \kern2px \sin\left(2\pi \kern1px(f_0+f_A\kern2px x_0)\cdot t\right)$$*Tho it may vary, even if very slowly.*<br>*And if it does, we need to account for each little, infinitesimal, variation, to do so we need an integral*. 


So this is a frequency modulated signal and we know that the bandwidth that we obtain is infinite, but if the maximum frequency of the signal ($f_{S_{MAX}}$) is much smaller than the base frequency ($f_0$) then we can approximate in this way the bandwidth of the **FM signal** which is:<br>![[Pasted image 20230719105215.png]]

- Where: 
	- $\Delta f_{MAX} = f_A \cdot x_{MAX}$.
	- And $f_A$ comes from: $f(t) = f_0\left(1+\frac{f_A}{f_0}x(t)\right)$
- The complete FM circuit has this topology here: ...
- We can say that this kind of readout electronics, since it transforms a variation of the input quantity into a variation of frequency is a very robust solution to **reject noise**.
- ***What do we mean with bandwith of a signal?***
	- The bandwidth of a signal refers to the range of frequencies contained within that signal.<br>In the context of signals, such as audio or electromagnetic waves, it represents the difference between the highest and lowest frequencies present in the signal.
	- Mathematically, the bandwidth ($B$) is often defined as:
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