##### ***Remeber***:

> We can model an **AT-Cut Quartz**, which is a special cut along a [[SaM - Crystallographic Axis|crystallographic axis]] of a quartz, like so:<br>![[Pasted image 20230720170030 1.png|500]]
> - $C_E$ is the capacity brought by placeing two metal layers on top of the quartz.
> - We have given some common values for the **electromechanical equivalent**, considering $\omega = 10 \ \text{MHz}$:$$\begin{array}{l}   L_{eq} = 100 \ \text{mH}  \\[2px]  C_{eq} = 15 \ \text{fF}  \\[4px]  R_{eq} = 20 \ohm \end{array}$$**Remember**: $1 f = 10^{-15}$.
> - The cut has a precise orientation with respect to the lattice. 
> - Therefore, we know also which one of the piezoelectric coefficient has to be taken into account in order to describe the phenomena.

> We can plot the reactance, given that: $Z_{eq} = C_E \parallel (L_{eq} + R_{eq} + C_{eq})$ and for sempliciity we will consider:
> 1. $R_{eq} = 0$
> 2. Instead of plotting $Z_{eq}$ (the impedance) we will plot $X_{eq}$ (the **reactance**) where: $Z_{eq} = j X_{eq}$.
> 
> Here is the unsimplified formula of $X_{eq}$:$$X(j\omega) = - {{1- \omega^2 L_{eq} C_{eq} \over 1 - \omega^2 L_{eq} {\large {C_E \kern2px C_{eq} \over C_E + C_{eq}}}}} $$And if we consider that $C_E \ll C_{eq}$, and for low frequencies, we can simplifiy to:$$X_{eq} = {1 \over \omega  \kern2px C_{\kern-2pxE}}$$
> And here's the simple plot:<br>![[Pasted image 20230720170052 1.png|333]]
> - So the behavior of the quartz is the normal behavior of the capacitance

> Now let's define two imporant frequencies:$$\omega_s = \sqrt{{1 \over L_{eq} \kern1px C_{eq}}}$$And:$$\omega_p = \sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq} \kern1px C_{eq}}}$$This is what happenes at high frequency when $w=w_s$ and $w = w_p$:<br>![[Pasted image 20230720170111 1.png]]
> - ==In a small frequency interval, we have a huge shift in amplitude, and the behavior of the quartz becomes normal behavior of an **inductance**, than returns to that of a **capacitance**==. 
> - $w_p$ and $w_s$ are very close since $C_E \gg C_{eq}$.
> - We define for convinience:$$A(\omega) = {1 - \frac{\omega^2}{\omega_s^2} \over 1 - \frac{\omega^2}{\omega_p^2}}$$And outside this really small range $[\omega_s ,\ \omega_p]$ the value of $A(\omega) \simeq 1$.

> We have seen some numeric examples: #IMPORTANTE 
> - The percentage difference (calculated like a relative error) of $\omega_s$ and $\omega_p$ is $10^{-5} \, \%$, (really small difference between $\omega_s$ and $\omega_p$).
> - So let's take for example $\omega_s = 10 \ \text{MHz} = 10{\small^{'}}000{\small^{'}}000 \ \text{Hz}$ then $\omega_p = 10{\small^{'}}000{\small^{'}}100 \ \text{Hz}$.

> If we perform some calculations, we will find that: $t = \frac{\lambda_w}{2 \pi}$.
> But actually due to some errors the **real beahaviour** is a bit different:$$t = {\lambda_w \over 2}$$==So if a slice of **AT-Cut Quartz**, the thickness of the slice will decide the wavelength==. #IMPORTANTE 

> We have considered $R_{eq} = 0$, and to recap here is the $|Z(\omega)|$ plot that we have seen:<br>![[Pasted image 20230926190017.png]]
> *But what if $R_{eq} \neq 0$?*
> ⇒ Then $Z_{eq}$ is not a pure reactance anymore, it has real and imaginary part:<br>![[Pasted image 20230720170218.png]]
> - The **red line** is an inducatance with a **greater** $R_{eq}$ with respect to the **blue line**.<br>So: $R_{eq_{\kern2px \text{RED}}} \gt R_{eq_{\kern2px \text{BLUE}}}$
> - The width of the arc that forms (looking at the amplitude plot) is related to the $Q$-factor.<br>The $Q$-factor decreases if $R_{eq}$ increments.

> Even if we take an $R_{eq}$ really small, so a small window in which the device behaves like an inductance, still the amplitude $|Z|$ changes a lot:<br>![[Pasted image 20230926190911.png]]
> - So we have a special component that acts like a conductance, then like an inductance (for a small range of frequency) and then again like a conductance.
> - ==More important the small range in which it acts as an inductance is set by the **physical** properties of the quartz, that define $\omega_s$ and $\omega_p$==.
> - **NOTE**: the small range is NOT $[\omega_s ,\ \omega_p]$, it is **even smaller**, it is contained in this range and the actual range depends on $R_{eq}$.<br>If $R_{eq}$ is small enough we consider to have an inductance-behaviour exactly in this range $[\omega_s ,\ \omega_p]$.

---

So I take as an example the so-called **AT-Cut quartz**. 
![[Pasted image 20230720170030.png|]]
- The cut has a precise orientation with respect to the lattice. 
- Therefore, we know also which one of the piezoelectric coefficient has to be taken into account in order to describe the phenomena.
- $C_E$ is the capacity brought by placeing two metal layers on top of the quartz.

We evaluate $Z_{eq} = C_E \parallel (L_{eq} + R_{eq} + C_{eq})$, but we consider $R_{eq} = 0$ (it is typically very small).
So it is just the imaginary part:
![[Pasted image 20230720170043.png]]

So we can plot $X(j \omega)$:
![[Pasted image 20230720170052.png]]
- So the behavior of the quartz is the normal behavior of the capacitance.

But even if the values are extreamely low, we can define:$$\omega_s = \sqrt{{1 \over L_{eq} C_{eq}}}$$And more importantly:$$\omega_p = \sqrt{{C_E + C_eq \over C_{E} L_{eq} C_{eq}}}$$
This is what happenes at high frequency when $w=w_s$ and $w = w_p$.
![[Pasted image 20230720170111.png]]
- $w_p$ and $w_s$ are very close since $C_E \gg C_{eq}$.
- We define for convinience:$$A(\omega) = {1 - \frac{\omega^2}{\omega_s^2} \over 1 - \frac{\omega^2}{\omega_p^2}}$$
- And outside this really small range $[\omega_s ,\ \omega_p]$ the value of $A(\omega) \simeq 1$.

Let's see some numeric examples:
![[Pasted image 20230720170127.png]]
![[Pasted image 20230720170146.png]]
- $\sqrt{K \over m}$ is defined as the **mechanical natural frequency**, it is often used and found in mass-spring-dumper system.

But we can write $K$ the elastic coefficient as:$$K = {T_{11} A \over \varepsilon_{11} t}$$Since:
- $T_{11} = \frac{F}{A}$ ⇒ $T_{11} A = F$.
- $\varepsilon_{11} = {\Delta x \over x}$ and in this case the variation quantity $x$ is $t$ ⇒ $\varepsilon_{11} t = \Delta t$
- ==**NOTE**: This coefficinents are given by the **cut** "type"==.

So we obtain the (inverse) most common Hooke's Law: $K = \frac{F}{\Delta x}$

Also:$$m = \rho V = \rho A t$$Where: 
- $\rho$ : density.
- $V$ : volume.

So we can write $\omega_s$ as $\frac{1}{t}\sqrt{c_{11} \over \rho}$, as you can see here:
![[Pasted image 20230720170153.png]]
- We find that: $t = \frac{\lambda_w}{2 \pi}$
- But actually due to some errors the **real beahaviour** is similar but it is:$$t = {\lambda_w \over 2}$$

==So if a slice of **AT-Cut Quartz**, the thickness of the slice will decide the wavelength==.
This is an extreamly convinient property.

If $R_{eq} = 0$: (as we have seen):
![[Pasted image 20230926190017.png]]

*What if $R_{eq} \neq 0$?*
Then $Z_{eq}$ is not a pure reactance anymore, it has real and imaginary part:
![[Pasted image 20230720170218.png]]
- In red a greater $R_{eq}$ than in blue.
- The width of the arc that forms (looking at the amplitude plot) is related to the $Q$-factor.
- The $Q$-factor decreases if $R_{eq}$ increments.
- As I said before we wold require (usally) $R_{eq} \lt 20 \ohm$, otherwise strange phenomena can happen.
- If the phase does not change, then we will not have a change from capacitive-behaviour to inductive-behaviour, more on that later.

If the $Q$-factor is large enough, so if $R_{eq}$ is small enough, we will have a small frequency, in which the system behaves like an inductance, so the phase is kept at $90°$ for a bit, we can see it in the figure below:
![[Pasted image 20230926190549.png]]
- Even if this range is small, the amplitude $|Z|$ changes a lot (as we can see in the previous figure), so we have some liberty over the values $Z_{eq}$ can assume.

So we have a special component that acts like a conductance, then like an inductance (for a small range of frequency) and then again like a conductance:
![[Pasted image 20230926190911.png]]
- More important the small range in which it acts as an inductance is set by the **physical** properties of the quartz, that define $\omega_s$ and $\omega_p$.
- **NOTE**: the small range is NOT $[\omega_s ,\ \omega_p]$, it is **even smaller**, it is contained in this range and the actual range depends on $R_{eq}$.<br>If $R_{eq}$ is small enough we consider to have an inductance-behaviour exactly in this range $[\omega_s ,\ \omega_p]$.

---