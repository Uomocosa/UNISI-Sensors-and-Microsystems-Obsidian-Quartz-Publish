##### ***Remeber***:

> A coaxial cable is used to reduce the [[SaM - Electrical Noise|electical noise]] on a **wire**, this is a simple structure:<br>![[Pasted image 20230718201110 1.png]]
> - A **coaxial cable**, it is essentially made of 5 layers:
> 	1. **Inner Conductor** or **Wire**.
> 	2. **1st Insulation**.
> 	3. **Outer Conductor** or **Elettromagnetic Shield**.
> 	4. **2nd Insulation.**
> 	5. **Outer Jacket** or **Durable Shield** (in particular this shield provides mechanical protection and shields the cable from environmental factors like moisture and physical damage).

> We can model the coaxial cable's capacitance this way:![[Pasted image 20230718201110 2.png]]
> - $C_G$ : **guard gapacitance**, which in this case is the cable capacitance.
> - $C_R$ : **reference capacitance**.
> - $C_S$ : sensor.
> - $R_{in}$: input resistance to front-end electroncis.
> - $C_P$ : parasitic capacitance (from the front-end electronics).
> - The cable capacitance is fixed, and it doesn't change, also this capacitance is for sure larger than before, because now I have a small distance between ground and the wire.
> - This is a good solution (*for electrical noise*), but we have still a big problem:<br>For a coaxial cable, we can imagine to have a value of capacitance $C_G$, which is $100 \frac{\text{pF}}{m}$ multiplied by the length $l$ of the cable, so if the the cable is long and $C_G$ is really big, it will "mask" the relativily small value of our sensor ($C_S$), we will lose a lot of sensitivity. #IMPORTANTE 
> - ==So this arrangement here is not good if the **$C_S$ sensor's capacitance is small** and if the **cable is long**==, so if $C_G \gg C_S$. #IMPORTANTE 
> - To put into prospective, for instance, $10$ meters of cable means $C_G \simeq 1 \text{nF}$, we have said that our $C_S$ in in the order of $0.1 \kern2px pF$, so ($10^{-13}$).<br>⇒ $C_G$ is **$10'000$ times larger than the capacitance of the sensor** $C_S$.
> - The same problem can also occurr if $C_R \gg C_S$, but we just need to change source in that case.

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_7.jpg]]

---
![[Pasted image 20230718201110.png]]
- Given a wire, we insulate it using an **insulating cylinder** which surrounds the wire.<br>And above this, on the outer surface we have a metallic network or **metallic shield**, which is placed all around, and it's grounded.
- The capacitance is fixed, and it doesn't change, also this capacitance is for sure larger than before, because now I have a small distance between ground and the wire.

This is a good solution, but we have still a big problem:<br>For a coaxial cable, we can imagine to have a value of capacitance $C_G$, which is $100 \frac{\text{pF}}{m}$ multiplied by the length $l$ of the cable, so if the the cable is long and $C_G$ is really big, it will "mask" the relativily small value of our sensor ($C_S$), we will lose a lot of sensitivity.
==So this arrangement here is not good if the **$C_S$ sensor's capacitance is small** and if the **cable is long**.<br>So if $C_G \gg C_S$==.

To put into prospective, for instance, $10$ meters of cable means $C_G \simeq 1 \text{nF}$, we have said that our $C_S$ in in the order of $0.1 \kern2px pF$, so ($10^{-13}$).
⇒ $C_G$ is **$10'000$ times larger than the capacitance of the sensor** $C_S$.

The same problem can also occurr if $C_R \gg C_S$, but we just need to change source in that case.

A **coaxial cable**, it is essentially made of 5 layers:
1. **Inner Conductor** or **Wire**
2. **1st Insulation**
3. **Outer Conductor** or **Elettromagnetic Shield**
4. **2nd Insulation**
5. **Outer Jacket** or **Durable Shield** (in particular this shield provides mechanical protection and shields the cable from environmental factors like moisture and physical damage)