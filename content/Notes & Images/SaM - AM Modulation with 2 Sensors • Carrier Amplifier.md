##### ***Remeber***:

> We have said that for reading a [[SaM - Types of Capacitive Sensors|capacitive sensor]], if the measured quantity varies slowly, we need a special [[SaM - Readout Electronics for Capacitive Sensors (FM & AM Oscillators)|modulation of the signal]].
> We have seen [[SaM - AM (Amplitude Modulation) Based on Oscillators|AM modulation]] and [[SaM - FM (Frequency Modulation) Based on Oscillators|FM modulation]], let's see now another option.
> Like for **AM modulation**, we will use **ungrounded** or **unreferenced** sensors.

> This time we'll use two capacitive sensors, mounted on a structure like this:<br>![[Pasted image 20230719105256 1.png|500]]
> - $|A| = \infty$ (ideal **op amp**).
> - $R_f$ is needed to reduce the effects of the **DC** errors of the amplifer.
> - $C_1$ and $C_2$ are [[SaM - Types of Capacitive Sensors|capacitive sensors]].<br>We will model them as: #NOT_SURE_ABOUT_THIS $$C_1 = {{C_0 \over 1 + x}}, \kern20px  C_2 = {{C_0 \over 1 - x}}$$
> - The output function is:$$V_{out} = V_g \left({Z_f \over Z_1} - {Z_f \over Z_2}\right)$$Where:
> 	- $Z_f = R_f \parallel {1 \over j \omega C_f} = {R_f \over 1 + j \omega R_f C_f}$
> 	- $Z_1 = {1 \over j \omega C_1}$
> 	- $Z_2 = {1 \over j \omega C_2}$

> If we perform the calculations, we find:$$V_{out} = V{\kern-4px {\small{g}}} \kern2px {R_f \over 1 + j \omega R_f C_f} (j \omega2 C_0 \kern2px x) $$Where:
> - $x \in [0,\ 1]$, also $x \ll 1$
> - $C_1 = {\large{C_0 \over 1 + x}}$
> - $C_2 = {\large{C_0 \over 1 - x}}$

> This will be the response of our circuit:<br>![[Pasted image 20230719105325.png|500]]
> - I have considered $- \frac{2 \kern2px C_0 \kern2px x}{C_f}$ **constant** in order to be able to study everything using these simple equations in the frequency domain.<br>⇒ So I need to consider that the frequency of the input $f_0$ is much larger than the maximum frequency of the signal, such that I can consider this quantity static during the analysis:$$f_0 \gg f_{S_{MAX}}$$
> - If I select a large value for this resistance $R_f$, then I can select the $f_0$ I prefer.
> - Also I have another constraint, if I select a value for $C_f$ too large with respect to $C_0$ than I'll have a very small signal.<br>⇒ So I'm obliged to select this value small enough to give enough sensitivity.
> - Even if I take $R_f$ extreamly big, the output will still be (approximated):$$V_0 \simeq V \cdot \frac{2C_0}{C_f}x$$

> If we use this circuit, ==we will lose the sign of $x$== in the output, since the output is a sinusoidal, while $x$ is a scalar value, we will see an example on this later.
> We need to recover the sign of $x$, which is the same as $$\operatorname{sign}(x) = \operatorname{sign}\left({V_{out} \over V_g}\right)$$Therefore, we need a circuit which is able to do two things:
> 1. ==Finds the output amplitude $V_{out}$==.
> 2. ==Being able to recover the phase, and distinguish if I have a $0°$ or $180°$==.
> 
> Here's the complete circuit, that can also recover the sign of $x$, using a **carrier amplifier**: <br>![[Pasted image 20230719105428.png|500]]

> Here's some interactive circuits:
> - [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3YBMBWEAOAnLAzBgbNmBgOyKKTbYAsIieIqykDApgLRhgBQAxrVc3whskGkOYx4CTiCrQMyDCOqI0iannI1IvfsyKJho8BkODYGKVfhh2xEGzkK0xbMmRU0yMFSp57OgDuRmL0IjQ+2lzB4eC+ISZm0QmRwnhocVEAhmkZYHjMnvoF6OCoHKhg1lCw8BiY9Uz5cKqe2FDgVlwA5rngxGHpeh1BfanYQ+JcAE59QkUg4p1dfBMZnrJohRn6tdb7tmz2WA0YVBhgyF4ikF41CMlri4PrO8kL81ubUFwAbiB4UKZZ4dCBVZioCQ1ZDvL6fYoSHoAoGA8BIEZcATtJZkGio-SIAD6gMJkEJAnqhKqVMgiGgVEJHEJRKQhOwsIRDHizVomIosg2YAGDGFiAEoLwxIZZIpGGZZMkdQGyE0yEZYGZVMl7NmYsE9AMIP0Ol14sN5tMoJ0vVRhtR5B2P3+qTtEUt+mWDBG0OSqSEhqEiF93MtFsMQYA9uBDPjZJB6rRjXTtLJo8JwPRisIuEA) (_Difference between $C_1$ and $C_2$ **low**, a more real case scenario_)<br>![[Pasted image 20240117201137.png]]
> - [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3YBMBWEAOAnLAzBgbNmBgOyKKTbYAsIieIqykDApgLRhgBQAxrVcyKIQ2SDSFQoseJE4Q22aGkTFkTWVVwDiGKL37N8IsSCOHYGGVfhh2xEUsI7siKskRhkmtDUhcA7sY0RqLiVL4BQeDhURJ+gaHRNNh4aEl6AIYiqeB4zFRognno4KgcqGDWIGwwMsR4JPhwuJWUGKiCVlwA5tlpYPV9BpLxQ2AxKWlmXABOQ0YFhvSdXXyTIAUbhVuSYNLWB7Zs9sfQDYXYxLJoV5doy9LcCTkhOZuji6b0n+9cAG4gPDBejjYG7cBwBgjKTISKfBbbMDFPy9IFfQHiJAjLgCbDo5hkGhowSIAD6QNJkFJAgwaFJlXpkEQ0CopI4pLJSFJ2DhiOKXnExUQOIoG02A3oyEGrmYRXJrKpNIwHKptXgJDwyDwKDZYA59Lw3NmwyMEjMEONMvAGGEEjiFtR4htGNokDSsv+6QkaPtEEqzA6I2gsMCoPRZvowtDMTtzokwoA9uBhMSNpBaa6IczfBtkyJcrt6DygA) (_~Ex.: with respect to the previous circuit, we invert the sing of $x$, in practice, we have swapped the capcacitances $C_1$ and $C_2$, the output has same amplitude but inverse sign_)<br>![[Pasted image 20240117201238.png]]

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_5.jpg]]

---

![[Pasted image 20230719105256.png]]
![[Pasted image 20230719105305.png]]

If we take $x \ll 1$ (which for proximity sensor should often be the case) we can simplify:<br>![[Pasted image 20230719105325 1.png]]
- I have considered $- \frac{2 \kern2px C_0 \kern2px x}{C_f}$ **constant** in order to be able to study everything using these simple equations in the frequency domain.<br>so I consider that the frequency of the input $f_0$ is much larger than the maximum frequency of the signal, such that I can consider this quantity static during the analysis.<br>Actually, we know that this change.
- So if will select a large value for this resistance $R_f$ in order to let me select the $f_0$ I prefer.
- Tho I have another constraint, if I select a value for $C_f$ too large with respect to $C_0$ than I'll have a very small signal.<br>⇒ So I'm obliged to select this value small enough to give enough sensitivity.
- Even if I take $R_f$ extreamly big, the output will still be (approximated):$$V_0 \simeq V \cdot \frac{2C_0}{C_f}x$$But I do have some liberty on $f_0$ (I do can choose $R_f$ big as I want, whithin some limits of course, #NOT_SURE_ABOUT_THIS )

![[Pasted image 20230719105428.png]]
- And you see that if $x$ changes its sign, what happens is that obviously the amplitude remains the same.<br>But the output will have a phase which is $180°$ different with respect to the input wave, which is $V_R$.
- Therefore, if we go back to the complete circuit, in this case, we need a circuit which is able to do two things:
  1. ==Finds the output amplitude $V_0$==.
  2. ==Being able to recover the phase, and distinguish if I have a $0°$ or $180°$==.

