##### ***Remeber***:

> If the signal measured by a [[SaM - Types of Capacitive Sensors|capacitive sensor]] has **DC components**, to "catch them" we need an **AC exitation**, as we have said [[SaM - Readout Electronics for Capacitive Sensors (FM & AM Oscillators)|before]].
> While if we have a **pure AC signal** (meaning with **no DC components**), so it has a spectrum like this:<br>![[Pasted image 20230719105735 1.png|333]]
> ⇒ Then **DC exitation is possible**.

> With a simple setup we can obtain the value of our measured quantity $x$:<br>![[Pasted image 20231119190855.png]]
> - $C_1 = {C_0 \over 1 - x}$
> - $C_2 = {C_0 \over 1 + x}$
> - The output will be, if we perform the calcualtions:$$V_{out} = {V_{DC}\over 2}(1-x)$$Where: the offset ${V_{DC}\over 2}$ can be corrected, and the final output $\left(-{V_{DC} \over 2}x\right)$ can be amplifed and inverted.

> We have seen the *example of a capacitive microphone*:<br>![[Pasted image 20230719105807 1.png|333]]
> The measured $C_S$ value is very small, and the nedded force $F$, to move the plate depends on: $$F \propto \frac{A}{h^2}$$Where $A$ and $h$ are the **physical dimensions** of the sensors ⇒ the minimum force which has to be overcome to move the movable plate is really small. #NOT_SURE_ABOUT_THIS 
> So the needed DC exitation to get a readable signal would be really high, $V_{DC}$ usually, it's a large value ($\sim 100 \kern2px V$). #IMPORTANTE #NOT_SURE_ABOUT_THIS 

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_7 1.jpg]]

---

![[Pasted image 20230719105735.png]]
![[Pasted image 20230719105742.png]]
- When we deal with **AC signals** and usually **high frequencies signals**, which means that the **spectrum of $x(t)$**: $X(f)$, so if the sensor measure has **no DC components**.<br>⇒ Then **DC exitation** is possible.
- While in [[SaM - FM & AM Oscillators (OLD)|AM and FM]] we had only **AC exitation**.
- A simple capacitive microphone uses this formula:$$C_{out} = \frac{C_0}{(1-x)}$$
- With a simple voltage divider using two sensors with "opposed signs", we have:$$V_{out} = \frac{V_{DC}}{2}(1-x)$$
- Also note that the offset of $\frac{V_{DC}}{2}$ can be removed, and the theoretical output value can become: $$V_{out} = -\frac{V_{DC}}{2}x$$Of course the output can be then amplified and inverted.
- $V_{DC}$ usually, it's a large value ($\sim 100 \kern2px V$). #IMPORTANTE 

---
Here we can see a typical solution in case of a capacitive microphone:
![[Pasted image 20230719105807.png]]
- Capacitive microphones have a **small mechanical load** represented by $R$.
- Since the $C_S$ value is very small, and the nedded force $F$, to move the plate depends on: $$F \propto \frac{A}{h^2}$$Where $A$ and $h$ are the **physical dimensions** of the sensors ⇒ the minimum force which has to be overcome to move the movable plate is really small.

---