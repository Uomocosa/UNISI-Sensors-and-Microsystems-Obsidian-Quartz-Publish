##### ***Remeber***:

> We defiened the [[SaM - AT-Cut Quartz|AT-cut quartz's impedance]] as:$$Z_{eq} = C_E \parallel (L_{eq} + R_{eq} + C_{eq})$$Where at $\omega = 10 \ \text{MHz}$, we gave some common values:$$\begin{array}{l}   L_{eq} = 100 \ \text{mH}  \\[2px]  C_{eq} = 15 \ \text{fF}  \\[4px]  R_{eq} = 20 \ohm \end{array}$$Then we defined:$$\omega_s = \sqrt{{1 \over L_{eq} \kern1px C_{eq}}}$$And:$$\omega_p = \sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq} \kern1px C_{eq}}}$$Giving us the **reactance formula** $\left(X_{eq} : Z_{eq} = jX_{eq}\right)$:$$X_{eq} = - {1\over\omega C_{\kern-2pxE}}{1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$$If we were to plot ${1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$ we would obtain this graph, as we [[SaM - AT-Cut Quartz|have already seen]]:<br>![[Pasted image 20230720170319 1.png|500]]
> - **Remember**: ==$Z_{eq}$, and consequently $\omega_s$ and $\omega_p$ depends on the [[SaM - Types of Cut Quartzes|type of cut]] of the quartz==.

> Actally this is an approximation, if we were to plot and model the real behaviour of the quartz we wold need an infinite numeber of $Z_{q_i}$ impedances in parallel to $C_{\kern-2px E}$:<br>![[Pasted image 20230720170338.png|500]]
> - If we work at a high frequency $(f \in [20 \ \text{MHz} \div 30 \ \text{MHz}])$, we need to consider this additional impedaces, after the first.
> - If we work at lower frequencies $(\lt 10 \ \text{MHz})$ we can consider just the first ($Z_{eq}$).

> We can write the relationships of the different components:$$\begin{array}{l}   L_{m_i} = {1 \over 8}{m \over k^2 d^2}  \\[5px]  C_{m_i} = {8 \over (i \cdot \pi)^2}k d^2  \\[4px]  R_{m_i} = {(i \cdot \pi)^2 \over 8}{\lambda \over k^2 d^2} \end{array}$$And also define each value for $\omega_{s_i}$ :$$\omega_{s_i} \approx i \cdot w_{s_1}$$However this is not very accurate

---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_4.jpg]]

---
We need the transverse propagation velocity $v_t$ and not the longitudinal one $v_l$, so:
![[Pasted image 20230720170312.png]]
- $Z_{eq}$ : is the equivalent impedance of the quartz we have found.
- $Z_m$ is a novelty and is the **mechanical impedance of the medium**, it is ==usually negligible== since the quartz is extremely light, with respect to the body it's mounted on.

And we have also seen that we can define $X_{eq}$ (for $R_{eq}=0$) as:
![[Pasted image 20230720170319.png]]
- Also we see again the plot of $X_{eq}$.
- You can see that the quartz behaves as the capacitance $C_{\kern-2pxE}$ (defined by the construction of the capacitance quartz), except for a small range where it acts as an inductance, this small range and inductance value is due to the parallel with $Z_{m}$, and it is decided by the **cut-type** and **quartz-type**.
- $Z_{q}$ : is the **real value of $Z_{eq}$** also considering $R_{eq}$. #NOT_SURE_ABOUT_THIS 

We can expand $Z_{q}$ as the parallel of an infnite number of impedances, like so:$$Z_{q} = Z_{E} \parallel Z_{q_1} \parallel Z_{q_2} \parallel \ldots \parallel Z_{q_\infty} $$
==**NOTE**: This is the real behavior of the quartz==

Each $Z_{q_i}$ can be considered as an open circuit expect for a small frequency range, where it resonates.

Where:
![[Pasted image 20230720170338.png]]
- The plot is a simplified version to understand what happens.<br>Again in this graph we have negleted the resitance.
- As you can see we have stopped at the first resonance, but if for any reason our frequency grows we will encounter another resonance, $\omega_{s_2}$, then $\omega_{s_3}$ and so on...
- If we work at high frequency ($20, 30$ **MHz**), we need to consider them.<br>If we work at low frequncy ($10$ **MHz**) we can consider just the first.

So we can write the relationships of the different components, and also define each value for $\omega_{s_i}$ :
![[Pasted image 20230720170346.png]]
- The first one, we already found is around $1 \over \sqrt{L_{eq}C_{eq}}$
- The others are around:$$n \cdot \omega_s$$With: $n \in \mathbb{N}$
- However this is not very accurate.
- **This is the real behavior of the quartz**.

---