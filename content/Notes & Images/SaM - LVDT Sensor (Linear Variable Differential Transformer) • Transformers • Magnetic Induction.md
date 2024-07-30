##### ***Remeber***:

> ***Formula used for transformers or magnetic induction***: #IMPORTANTE 
> A transformer with mutual inductance $M$ and two currents $i_1$ and $i_2$ flowing trough its two "branches", then we will have the two voltage drops equal to (in the frequency domain):$$\begin{align}&V_1 = j\kern2px \omega \kern1px M \kern1px i_2\\&V_2 = j\kern2px \omega \kern1px M \kern1px i_1\end{align}$$

> - Here is a scheme of an ***LVDT Sensor***:<br>![[Pasted image 20230719114148.png|333]]<br>![[Pasted image 20230719114202.png|333]]
> - The **primary winding** is the one here at center and two identical **secondary windings** at the opposite ends of the cylinder.
> - The **primary winding** (or coil) here is excited by an **AC voltage** such that a **magnetic field** is created.<br>The inner cylinder called the **core** is **ferromagnetic**.
> - When the sensor is in its reference position, the **core** is perfectly centered and symmetrical with respect to the **secondary windings**.<br>⇒ The **mutual inductance**, between the **primary** and each **secondary coils** is exactly the same when the **core** is in its reference position, so the output will be $0 V$.
> - If instead the **core** moves, then **the structure becomes unbalanced and the mutual induction changes**.<br>So one of the **mutual induction** between the **primary** and one of the **secondary windings** is increasing and the other is decreasing depending on the position of the **core**.

> Here is the **electric circuit**:<br>![[Pasted image 20230719114229 1.png|500]]
> - The output formula is: $$V_{out} = \frac{ j \omega R_Lk x E_1}{(R_1 + j\omega L_1)(R_2 + j\omega L_2)}$$Where:
> 	- $M_1 - M_2 = kx$ (linear approximation).
> 	- $R_2 = R_2' + R_2'' + R_L$
> 	- $L_2 = L_2' + L_2''$
> 	- ==Remeber that this model is valid for $f_s \ll f_{exc}$==, meaning that the mesurand $x$ must vary relatevely slowly to the exatitaion, so that we can consider $x$ constant to respect to the exatation signal $E_1$.

> Let's look at the [[Bode Plot|Bode plot]] of the transfer function $\frac{V_{out}}{E_1}$:<br>![[Pasted image 20230719114256.png|500]]

> - There is a zero in zero, and two poles one at $f_1 = \frac{1}{2\pi}\frac{R_1}{L_1}$ and one at $f_2 = \frac{1}{2\pi}\frac{R_2}{L_2}$.
> - If operate in "linear reagion" meaning with $f_{exc} \in \left[f_1 ,\ f_2\right]$, and we suppose (as it usually is) $R_L \gg R_1,\ R_2',\ R_2''$, so that $R_2 \gg R_1$ and $R_2 \approx R_L$ we can approximate:$$\frac{kxR_L}{R_2L_1 + R_1 L_2} \simeq \frac{kx}{L_1}$$Where, we defined:$$R_2 = R_2' + R_2'' + R_L\simeq R_L$$

> It will be wise to select $f_{exc} \simeq f_0$, so that the output will be in-phase ($\large{\varphi}_{\normalsize V_{out}} \simeq \large{\varphi}_{\normalsize E_1}$) with the input, where:$$f_0 = {1 \over 2\pi} \sqrt{{R_1 R_2 \over L_1 L_2}}$$

> *What happens if $x \lt 0$?* ⇒ The initial phase is shifted by $-180°$ and the same is true for the phase at $f_0$.<br>We will lose the sign of $x$ at the output.
> If we draw the output I find something like this:<br>![[Pasted image 20230719114323.png|333]]
> - We can approximate this sensor as linear if we stay in the "linear range" defined by $[-x_{LIN},\ +x_{LIN}]$.
> - But sometimes it is accepted to work in the **extended range**.

> To recover the sign of $x$ we need a [[SaM - Carrier Amplifier|carrier amplifier]]:<br>![[Pasted image 20230719114348.png|500]]
> - Remeber that the exation $E_1$ is an **AC** signal, and as [[SaM - Carrier Amplifier|we have seen]] that after a **carrier amplifier**, there is a need of a [[SaM - Low Pass Filter|LPF (Low Pass Filter)]], which gives us finally a **DC** signal.
> - The final outptut will be the amplitude of $V_{\text{out}}$ multiplied by the sign of $x$, also it will be a **DC signal**, or at most **a slow varying signal**.
> - *There exists some IC (integrated circuits) which embed all of this and are ready to be used with a sensor*.
> - We have also seen how to avoid the need for a carrier amplifier, using a [[SaM - 5 Wires LVDT (Linear Variable Differential Transformer)|5 wires strucuture]].

> #IMPORTANTE [[SaM - Characteristics of Different Kinds of LVDTs|Characteristics of Different Kinds of LVDTs]]

---
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_3.jpg]]

---
##### LVDT Sensor
***Linear Variable Differential Tansformer***.
It is another **displacement sensor** as the others that we have seen, but in this case, we have a **contact measurement system**.
![[Pasted image 20230719114140.png]]

I'll show you the structure:
![[Pasted image 20230921161500.png]]
![[Pasted image 20230719114148.png]]
![[Pasted image 20230719114202.png]]
- The **primary winding** is the one here at center and two identical **secondary windings** at the opposite ends of the cylinder.
- The **primary winding** (or coil) here is excited by an **AC voltage** such that a **magnetic field** is created.
- The inner cylinder called the **core** is **ferromagnetic**.
- The **core** when the sensor is in its reference position, is perfectly centered and symmetrical with respect to the **secondary windings**.<br>⇒ The **mutual inductance**, between the **primary** and each **secondary coils** is exactly the same when the **core** is in its reference position, so the output will be $0 V$.
- If instead the **core** moves, then **the structure becomes unbalanced and the mutual induction changes**.<br>So one of the **mutual induction** between the **primary** and one of the **secondary windings** is increasing and the other is decreasing depending on the position of the **core**.

%%
![[Pasted image 20230719114206.png]]
%%

> ***Formula used for transformers***:
> A transformer with mutual inductance $M$ and two currents $i_1$ and $i_2$ flowing trough its two "branches", then we will have the two voltage drops equal to (in the frequency domain):$$\begin{align}&V_1 = j\kern2px \omega \kern1px M \kern1px i_2\\&V_2 = j\kern2px \omega \kern1px M \kern1px i_1\end{align}$$

Here is the **electric circuit**:<br>![[Pasted image 20230719114229.png]]
- So we have a first circuti which describes the exited core:
	- $E_1$ : the **AC exitation**
	- $L_1,\ R_1$ : the primary winding inductance and resistance.
	- $M_1,\ M_2$ : Mutual Inductances between $1$ and $2'$ and between $1$ and $2''$, which are the windings, these mutual inductances will change due to the position of the core.<br>The formulas governing these inductances are:$$\begin{align}&E_1 = (j \omega L_1 + R_1) \kern2px i_1 + j \omega (M_2 - M_1) \kern2px i_2\\&E_2= 0  = (j \omega L_2 + R_2) \kern2px i_1 + j \omega (M_2 - M_1) \kern2px i_2\\& M_2-M_1=k \kern1px x \kern15px \text{(linear approximation)}\end{align}$$NOTE:
		- The first two equations are simple voltage mesh (*In italiano "**maglie**"*), voltage equations. 
		- The third is a simple approximation taken arbitrarly.

Doing some calculation we get:
![[Pasted image 20230719114245.png]]
- The formula is a little wrong, there is one too much $R_2$, I rewrite it:$$V_{out} = \frac{ j \omega R_Lk}{(R_1 + j\omega L_1)(R_2 + j\omega L_2)}x$$
- As we have alredy said in other cases, this is valid for $f_s \ll f_{exc}$.


Therefore, we can draw the transfer function of this circuit:<br>![[Pasted image 20230719114256.png]]
- If we suppose (as it usually is) $R_L \gg R_1,\ R_2',\ R_2''$, we can approximate:$$\frac{kxR_L}{R_2L_1 + R_1 L_2} \simeq \frac{kx}{L_1}$$Since remember that we defined:$$R_2 = R_2' + R_2'' + R_L\simeq R_L$$
- As we can see from the output formula:$$V_{out} = \frac{ j \omega R_Lkx}{(R_1 + j\omega L_1)+(R_2 + j\omega L_2)}$$There is a zero in zero, and two poles one at $f_1 = \frac{1}{2\pi}\frac{R_1}{L_1}$ and one at $f_2 = \frac{1}{2\pi}\frac{R_2}{L_2}$.


**NOTE**: the phase is equal to $0$ only in one point (this is kinda exagerated but you get the point):<br>![[Pasted image 20230719114308.png]]
- So it will be wise to select $f_{exc} \simeq f_0$, so that the output will be in-phase with the input.

*We have considered $x$ as greater than $0$, what happens if $x \lt 0$?*
⇒ The initial phase is shifted by $-180°$ and the same is true for the phase at $f_0$.
![[Pasted image 20230921162128.png]]
- We will lose the sign of $x$ at the output.

So if we draw the output obviously I find something like this:
![[Pasted image 20230719114323.png]]
- It is simmetrical.
- We can approximate this sensor as linear if we stay in the "linear range" defined by $[-x_{LIN},\ +x_{LIN}]$.
- But sometimes it is accepted to work in the **extended range**.

![[Pasted image 20230719114348.png]]
- Remember that the carrier amplifier is a structure which performs an amplification but also a comparison with the phase of the input signal, in order to understand if there is a shift of 180 degrees or not.
- After this since usually the carrier amplifier gives a signal which is no more AC.<br>⇒ Then we need a **low pass filter**.
- The final outptut will be the amplitude of $V_{\text{out}}$ multiplied by the sign of $x$, also it will be a **DC signal**, or at most **a slow varying signal**. 
- *There exists some IC (integrated circuits) which embed all of this and are ready to be used with a sensor*.