##### ***Remeber***:

> ==If a [[SaM - Ultrasonic Waves|wave]] travels in a homogeneous medium, nothing happens==, let's see what happens if the medium in not homogeneus.
> First we need the definition we have given to the [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|acustic impedance]]: #IMPORTANTE  $$Z = \rho \cdot v_l$$

> Suppose we have two materials represented by two different acustic impedances:<br>![[Pasted image 20230925185349.png|500]]
> - Here you can see the phenomena of reflection, part of the wave bounces back, with a different propagation velocity ($v_r$)
> - So we define:$$\begin{array}{l} v_i & \textit{(intial velocity of the wave)} \\[3px] v_{\tiny R} = \Gamma_{\tiny V} \cdot v_i & \textit{(velocity of the reflected wave)}  \\[3px] v_{\tiny T} = T_{\tiny V} \cdot v_i  & \textit{(velocity of the transmitted wave)} \\[3px] T_{11_i}  & \textit{(intial stress over the i-th dimension)} \\[3px] T_{11_{R}} = \Gamma_{\tiny T} \cdot T_{11_i} & \textit{(reflected wave's stress)} \\[3px]  T_{11_{T}} = T_{\tiny T} \cdot T_{11_i}   & \textit{(transmitted wave's stress)} \end{array}$$And:$$\begin{array}{l} T_{\tiny V} = {\huge{2 Z_1\over Z_1 + Z_2}}  & \textit{(transmitted coefficent for the velocity)} \\[7px] 
T_{\tiny T}  =  {\huge{Z_1-Z_2\over Z_1 + Z_2}}  & \textit{(transmitted coefficent for the stress)} \\[7px] 
\Gamma_{\tiny V}  = {\huge{2 Z_2\over Z_1 + Z_2}}   & \textit{(reflected coefficent for the velocity)} \\[7px] 
\Gamma{\tiny T}  =  {\huge{Z_2-Z_1\over Z_1 + Z_2}}  & \textit{(reflected coefficent for the stress)}
\end{array}$$
> - Keep in mind that ==we have considered many idealities (as always) and an **infinite plane**, and completely smooth surface of the plane==

> Up till now we have supposed:
> - An infinite smooth plane on which the [[SaM - Ultrasonic Waves|wave]] reflects.
> - A [[SaM - Planar Waves or Plane Waves|planar wave]], with direction $x_1$ perpendicular to the smooth plane.
>
> Suppose now the wave $(v_{i},\ T_{11_i})$ hits the plane with an angle $\theta_1$, called "***incident angle***", then we have that the resulting **transmitted wave** $(v_{\tiny T},\ T_{11_T})$ and **reflected wave** $(v_{\tiny R},\ T_{11_R})$ are "tilted" like so<br>![[Pasted image 20230720162211.png]]Where:$$\begin{array}{l}  \theta_2 = \theta_1  \\[3px]  {\large{\frac{\sin \theta_3}{Z_2} = \frac{\sin \theta_1}{Z_1}}} \end{array}$$

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_2.jpg]]

---
==If a [[SaM - Ultrasonic Waves|wave]] travels in a homogeneous medium, nothing happens==.
Instead when the wave encounters a **surface which separates an homogeneous medium and another homogeneous medium** (with different characteristics), then that could be a reflection.
Let's see how to quantify the phenomena of reflection:
![[Pasted image 20230720162047.png]]
- To do this, we have to introduce the **acoustic impedance**.
- So acoustic impedance is like a generalized impedance.
- The ***flow quantity*** (represented as a current) is the speed of the particles, which are vibrating and give the propagation of the wave.
- Whereas the ***effort quantity*** (represented as a voltage) is the **stress** ($T$), or in fluids the **pressure** ($P$).
- So the power ($P$) of the wave would be for us the product of this two quantity.

So we refer to this simple plane wave:
![[Pasted image 20230720162054.png]]
- So you will have uniform speed, preassure and stress.
- **NOTE**: $V_{1F}$ represents "how fast the wave changes form", the propagation speed is stille $v_l$.

So we can say, using ***Hooke's law***:
![[Pasted image 20230925184638.png]]
- We change the derivative since integating $T_{11}$ over time or space is similar, except it is scaled.

So the impedance is equal to:
![[Pasted image 20230925184942.png]]
- $\rho$ is the density as usual.
- So the impedance can be written in this two ways.
- $B = c_{11} = \frac{P}{\Delta V \over V}$ : Bulk modulus ($V$ in the formula is volume)

So suppose we have two materials represented by two different acustic impedances:
![[Pasted image 20230925185349.png]]
- Here you can see the phenomena of reflection, part of the wave bounces back, with a different propagation velocity ($v_r$)
- It is important that the propagation of the wave is perpendicular to the surface separating $Z_1$ and $Z_2$.
- $T_T$ : transmission coefficient for velocity; the ratio between the starting preassure and the pressure of the wave passed through $Z_2$.<br>(It's a pure number)
- $T_v$ : similar to $T_T$ is a ratio but this time between the propagation velocity.
- $\Gamma_v$ is the equivalent of $T_v$ but for the reflected wave, same for $\Gamma_T$ and $T_T$.

We define these coefficient, so that we can describe the "***transmitted***" and "***reflected***" part of the wave in terms of $v_i$ and $T_{11_{i}}$.
![[Pasted image 20230720162152.png]]
- $v$ in this formulas are proagation velocities.
- $\Gamma_v$ and $\Gamma_T$ : **reflection coefficients** for propagating velocity and stress (indicated by the pedicies $_v$ and $_T$, $\Gamma$ stands for "reflected".
- $T_v$ and $T_T$ : **transmitted coefficients** for propagating velocity and stress (indicated by the pedicies $_v$ and $_T$, the variable name $T$ stand for "transmitted"

We have considered many idealities (as always) and an **infinite plane**, completely smooth:
![[Pasted image 20230720162159.png]]

---

But I have a different incident angle, which means that I have this is the incident wave:
![[Pasted image 20230720162211.png]]
- So in this case here, if I call these angles: $\theta_1$, $\theta_2$, $\theta_3$.<br>We know that $\theta_1 = \theta_2$
- While:$$\frac{\sin \theta_3}{Z_2} = \frac{\sin \theta_1}{Z_1}$$