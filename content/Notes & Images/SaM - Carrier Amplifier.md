![[Pasted image 20230719105500.png]]
- $\phi$ or $\phi(V_g)$ is defined as $\operatorname{sign}(V_g)$.
- If $\phi$ is **high**, the switch $S_1$ is **ON**, and $S_2$ is **OFF**. 
- If $\phi$ is **low**, $S_1$ is **OFF**, and $S_2$ is **ON**. 
- **NOTE**: The resistance between $+$ and ground can assume any value ($R$, not just $R_1$).

This amplifier changes the sign of the input signal $V_0$, based on the sign of the signal $V_g$, so we will obtain as output signal $V_0' = V_0 \cdot \operatorname{sign}(V_g)$ 
![[Pasted image 20230719105515.png]]
- So if $V_0$ is "in phase", meaning it has the same sign as $V_g$ ⇒ $V_0'$ will be positive, otherwise if it is "not in phase", $V_0'$ will be negative.

If we wish to just get the sign of $V_0'$, so to know if $V_g$ and $V_0$ are "in phase", we can use an [[SaM - Low Pass Filter|LPF (Low Pass Filter)]]:
![[Pasted image 20230719105524.png]]

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_6.jpg]]

---