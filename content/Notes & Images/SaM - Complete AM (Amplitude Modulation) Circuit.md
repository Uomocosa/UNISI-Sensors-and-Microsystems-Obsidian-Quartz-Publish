##### ***Remeber***:

> This is the complete circuit for **amplitude modulation** with **differential capcitance sensors**:<br>![[Pasted image 20230719105428.png|500]]
> - So differential because the capacitances are:
> 	- $C_1 = \frac{C_0}{1+x}$
> 	- $C_2 = \frac{C_0}{1-x}$
> - $R_f$ is needed to reduce the effects of DC errors of the amplifier.
> - Let's explain each stage:
> 	1. We have a first conversion of the quantity $x$ into a **capacitance**, done by the sensors $C_1$ and $C_2$, both sensors are **differential sensors**, and we suppose them to be the same type of sensors, only mounted in "opposite directions". 
> 	2. Then we have a first stage formed by a generator of AC voltage ($V_g$) and an [[SaM - FM & AM Oscillators (OLD)|oscillator]] ($A$).<br>In this stage we convert the capacitance (of the sensors $C_1$ and $C_2$) into the amplitude, that means that we scale the amplitude of the sine generated by $V_g$ by the capacitance of the sensors, and we mantain the same frequency.<br>In this particular example we have taken the phase of the sine signal ($V_g$) at a **fixed frequency** ($f_0$).<br>The formula at this stage is:$$V_0 = -{2C_0\over C_f}|x|$$
> 	3. This last part here, formed by the [[SaM - Carrier Amplifier|carrier amplifier]] followed by the [[SaM - Low Pass Filter|Low Pass Filter (LPF)]], is needed to recover the amplitude and the phase, specifically with the carrier amplifier we recover the phase, (the output will be positive if $x$ and $V_g$ have the same sign, or negative otherwise) and with the low pass filter we will obtain a **DC** output that depends on the sensors' capacitances.<br>So at the end, we can have a low frequency voltage, which follows $x$.<br>So the output ($\text{OUT}$) is ready to be, for instance, acquired by an **AC-DC** (Analog to Digital Converter).

---

> - The output $\left(V_0\over V_g\right)$ of the second part (before the carrier amplifier), has this form:<br>![[Pasted image 20230719105436.png]]
> - ${1 \over 2\pi R_f C_f}$ is the lower frequency limit, defined by the [[SaM - Charge Amplifier|feedback impedance]], our frequency $f$ must be higher than this.
> - I put $|x|$ in the formula, because I'm dealing with the module, I can't tell just by looking at the output $V_0$ if $x$ is positive or negative.<br>==And this is the reason why we need the **carrier amplifier**, since we lose the sing of $x$==.

---

![[Pasted image 20230719105436.png]]
- ${1 \over 2\pi R_f C_f}$ is the cutoff frequency.
- I can put $|x|$ in the formula, because I'm dealing with the module. 
- If $x$ larger than $0$, then it means that I start from a positive phase, $90°$, then I go to a $0°$ phase.
- Instead, if, so this is $x$ smaller than $0$, so if I have $x$ negative, obviously I start from $-90°$, then I go to $-180°$. 

*So what happens?* 
![[Pasted image 20230719105450.png]]
- No matter the sign of $x$ the output $V_g$ will be the same, so it depends on $|x|$.<br>⇒ I need to recover the phase for the sign of $x$. 
- To recover the phase, I need the reference signal ($x$).<br>⇒ So I need a circuit able to compare the phase of the input signal with the phase of the output signal, in order to understand if they are in phase or out of phase. 

There are many solution for this problem, ==we have seen the **low frequency** solution==: the [[SaM - Carrier Amplifier|Carrier Amplifier]]:<br>![[Pasted image 20230719105500.png]]
- This amplifier changes the sign of the input signal $V_0$, based on the sign of the signal $V_g$, so we will obtain as output signal $V_0' = V_0 \cdot \operatorname{sign}(V_g)$ 

---

***Complete AM Circuit***:<br>![[Pasted image 20230719105536.png]]
- **NOTE**: This is the first circuit we have seen, where the ouptut is dependent on $|x|$ instead of $x$
- Since we have supposed to have $1 + m x(t)$ and not just $x(t)$, then $1 + m x(t)$ cannot get negative and we don't need any more circuitry, of course if $x_{MIN} > -1$ (acceptable condition #NOT_SURE_ABOUT_THIS )
- In case we don't have the $1$ in the formula, and $x$ can get negative, we need all the information related to the amplitude, and the information related to the phase.<br>Otherwise the simple initial system here is fine.
- If I want to have a better (larger) dynamic of the output I can correct the $1$ (which is fixed, so it doesn't carry information), and in this case $x$ can go below $0$ and I need the previous circuit as well to recover the sign.
- At the end we can see a simple **AC-DC Converter** (*Alternating Current to Direct Current Converter*) (a "peak" or "envelope", or "average rectified") circuit.

[Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAGMQAWPcFHsPrx5UY8SClKSp0siAYxinXJwEpmeAnmJRYkVhzAZCIQpxB8epqDrGQZ9yXOzRClbCUJwwGu9tF6WACdwI3BjCzDrMDgWAHcQ4zBE0KtIOISTM0NEwTT4iKTzDUyodIirAs4zNIBDDLAq8wwUcEb+JCYkaNs5fzh3N2xcYkI8BAwwbAgqbvgy5tazSur0gX5BbKFzMuKGsyHExpQWAHN6z3riFpEWADcuHjQebi2ZrlprEWgEU4fzfD+KE4IlKZxeVWekJBaXu4PBPHcwnA72o0O+v02wJmoSU11K+WK2Dw+3cICJS1WgkRGWpx3yC3JRQRxNKdU2jMwLUZ7TkYC6tio8l0XjUhCwigwcEIhGwCCQM1sOwRkCWhJZeSZ5gQ4UJKvxNL17NG+s2KG1BpWwVN5oiZuMCrSBlCyk1Lq+tgcDl50FFGGISWwGDwhGicvI-n0f2pazJxvdYk99l60EUuFccrFQLD110rAA9sgSlRgcR+F9plxC9gQlFyNgWEA) :<br>![[Pasted image 20231201154735.png]]
- Here is a simple circuit and as se can see if we change the value of the capacitance of the sensor, we are moduling the **amplitude** of the output, while the **phase** $f_0$ is decided by the **AC voltage source** ($V_g$)

So we summarize what we have seen when analyzing the complete circuit for amplitude modulation:<br>![[Pasted image 20230719105428.png]]
1. We have a first conversion of the quantity $x$ into a **capacitance**, and this is the sensor here, in this case differential. 
2. Then we have a first stage including this, which is an **oscillator**, a generator of AC voltage, and with this stage here, we convert the capacitance into the amplitude, and the phase in this case, of the sine signal at a fixed frequency $f_0$. 
3. This last part here, is needed to recover the amplitude and the phase. 
- So at the end, we can have here a voltage, a low frequency voltage, which follows $x$, and so it is ready to be, for instance, acquired by an **AD** (Analog to Digital Converter). 

---