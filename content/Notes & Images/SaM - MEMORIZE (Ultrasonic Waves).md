##### List of things to memorize:
![[SaM - Ultrasonic Waves]]

---
###### [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation]]
- ***Elastic waves***: _propagates in solids_.<br>_These are also called **pressure wave or stress wave** and are related to the **elastic behavior** of solids_.
- ***Acoustic waves*** : _propagates in fluids_.<br>_Air and human tissues are considered fluids_.
- ***How we defined a simple wave funtion***:
	1. Take a small cube:<br>![[Pasted image 20230719131407.png|333]]
	2. Define:
		- Small volume of the cube: $\Delta V = dx_1 \cdot dx_2 \cdot dx_3$
		- [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|Stress]]: $T = {F \over A}$
		- [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|Strain]]: $\varepsilon_{kl} = \frac{1}{2} \left( \frac{\partial u_k}{\partial x_l} + \frac{\partial u_l}{\partial x_k} \right)$
		- Second Newton's law: $F = m\cdot a$.<br>We will consider $F = \left< F_1 , 0 , 0 \right>$ for simplicity.
		-  [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]]: $T_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}c_{ijkl}\cdot\varepsilon_{kl}$
	3. The force $(F_1)$ can be found in two ways: from stress $(F = T \cdot A)$ : $$\begin{array}{l} F_1   & = & T_{11} (x_1+dx_1,\ x_2,\ x_3) \cdot dx_2 \cdot dx_3 - T_{11} (x_1,\ x_2,\ x_3) \cdot dx_2 \cdot dx_3 \kern5px + \\ & + & T_{12} (x_1,\ x_2+dx_2,\ x_3) \cdot dx_1 \cdot dx_3 - T_{12} (x_1,\ x_2,\ x_3) \cdot dx_1 \cdot dx_3 \kern5px + \\ & + & T_{13} (x_1,\ x_2,\ x_3+dx_3) \cdot dx_1 \cdot dx_2 - T_{13} (x_1,\ x_2,\ x_3) \cdot dx_1 \cdot dx_2 \end{array}$$And from the Second Newton's law $(F = m\cdot a)$ :$$\begin{array}{l} F_1 & = & \ddot u_1 \cdot   (\rho \cdot \Delta V)        \\ & = & \rho \kern2px \ddot u_1 \kern2px dx_1 \kern2px dx_2 \kern2px dx_3 \end{array}$$
	4. Calculate the **wave equation**:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$
- ***Terminology***:
	- $x_i$ is the $i$-the axis on which ==the waves propagates==. #NOT_SURE_ABOUT_THIS 
	- While $\vec u$ defines the ==direction where the particles that compose the wave move==. #NOT_SURE_ABOUT_THIS 

---
###### [[SaM - Planar Waves or Plane Waves]]
- ***A plane [[SaM - Ultrasonic Waves|wave]] propagates only in a single direction***:<br>![[Pasted image 20230719131543 1.png|333]]
- ***Formula***:$${\partial u_i \over \partial x_2} = {\partial u_i \over \partial x_3} = 0$$
- ***A planar wave in an [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic material]] (so that we can use the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor]])***:$$\begin{array}{l}  \rho \ddot u_1 =  c_{11}{\partial^2 u_1 \over \partial x_1^2}  \\[3px]  \rho \ddot u_2 =  c_{44}{\partial^2 u_2 \over \partial x_1^2}  \\[3px]  \rho \ddot u_3 =  c_{44}{\partial^2 u_3 \over \partial x_1^2} \end{array}$$
- ***Terminology***:
	- $x_i$ is the $i$-the axis on which ==the waves propagates==. #NOT_SURE_ABOUT_THIS 
	- While $\vec u$ defines the ==direction where the particles that compose the wave move==. #NOT_SURE_ABOUT_THIS 
	- If we look at the definitions of [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave]] and [[SaM - Transverse Waves or Shear Waves|transverse wave]], we can say that the planar wave is a combination of the two.

---
###### [[SaM - Longitudinal Waves or Compressive Waves]]
- ***In a longitudinal wave the displacement of the particles are parallel to the propagation of the wave***<br>***So: $\vec u \parallel \vec x$*** :<br>![[Pasted image 20230719131609.png|500]]
- ***Formulas (in an [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic material]])***:$$\begin{array}{l}  \rho \ddot u_1 =  c_{11}{\partial^2 u_1 \over \partial x_1^2}  \\[0px]  \rho \ddot u_2 = 0  \\[3px]  \rho \ddot u_3 = 0 \end{array}$$
- ***Terminology***:
	- $x_i$ is the $i$-the axis on which ==the waves propagates==. #NOT_SURE_ABOUT_THIS 
	- While $\vec u$ defines the ==direction where the particles that compose the wave move==. #NOT_SURE_ABOUT_THIS 

---
###### [[SaM - Transverse Waves or Shear Waves]]
- _Pure **transverse waves** are possible only in **solids**_.
- ***In a shear wave the displacement of the particles are perpendicular to the propagation of the wave***<br>***So: $\vec u \perp \vec x$*** :<br>![[Pasted image 20230719131619.png|333]]
- ***Formulas (in an [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic material]])***:$$\begin{array}{l}  \rho \ddot u_1 =  0  \\[3px]  \rho \ddot u_2 = c_{44}{\partial^2 u_2 \over \partial x_1^2}  \\[3px]  \rho \ddot u_3 = c_{44}{\partial^2 u_3 \over \partial x_1^2} \end{array}$$
- ***Terminology***:
	- $x_i$ is the $i$-the axis on which ==the waves propagates==. #NOT_SURE_ABOUT_THIS 
	- While $\vec u$ defines the ==direction where the particles that compose the wave move==. #NOT_SURE_ABOUT_THIS 
---
###### [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave]]
- ***Formula***:$$U_1(t, x_1) = U_{1F}\left(t - \sqrt{\rho \over c_{11}}\cdot x_1\right) + U_{1B}\left(t + \sqrt{\rho \over c_{11}}\cdot x_1\right)$$
- ***In the same media we can have two velocity for a [[SaM - Ultrasonic Waves|wave]]***:$$\begin{array}{l}  \text{longitudinal velocity:}& v_{\small l} = \sqrt{c_{11} \over \rho}  \\  \text{transverse velocity:}& v_{\small t} = \sqrt{c_{44} \over \rho}    \end{array}$$
- ***We can define the "components" of a [[SaM - Planar Waves or Plane Waves|generic planar wave]] ($U_1 ,\ U_2 ,\ U_3$, primitives of $\vec{\ddot{u}}$)***:$$\begin{array}{l} \text{longitudinal:} & U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right) + U_{!B}\left(t + \frac{x_1}{v_l}\right)   \\[5px]   \text{transverse:} & U_2(t,\, x_1) = U_{2F}\left(t - \frac{x_1}{v_t}\right) + U_{2B}\left(t + \frac{x_1}{v_t}\right)  \end{array}$$
- ***[[SaM ~ Example of an Ultrasonic Wave Function • Sine Plane Wave|Sine plane wave example]]***:$$U_1(t,\, x_1) = A \sin\left(2\pi f_0\left(t-\frac{x_1}{v_l}\right)\right)$$
- ***Wavelength***:$$\lambda_w = {v_l \over f_0}$$
- ***Definition of wavelength in a sine plane wave***:<br>![[Pasted image 20230719131639 1 1.png|333]]
- ***Real World Measures***:
	- Usually: $v_{\small l} \approx 2v_{\small t}$
	- For *Air*: $v_l \sim 340 \, {\text{m} \over \text{s}}$.
	- For *Water*: $v_l \sim 1500 \, {\text{m} \over \text{s}}$.
	- For *Steel*: $v_l \sim 6000 \, {\text{m} \over \text{s}}$ and $v_t \sim 3000 \, {\text{m} \over \text{s}}$.
- ***Terminology***
	- $c_{11}$ and $c_{44}$ come from the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor for isotropic materials]].
	- $\rho$ is the density of the material.
	- This two velocities relate to the [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave]] and [[SaM - Transverse Waves or Shear Waves|transverse wave]].
	-  $U_1$ and $U_2$ are functions of any shape.
		- $U_{1F}$ and $U_{2F}$ : function of any shape that propagates **Forward**.
		- $U_{1B}$ and $U_{2B}$ : function of any shape that propagates **Backward**.

---
###### [[SaM ~ Example of an Ultrasonic Wave Function • Sine Plane Wave]]
- ***[[SaM ~ Example of an Ultrasonic Wave Function • Sine Plane Wave|Sine plane wave example]]***:$$U_1(t,\, x_1) = A \sin\left(2\pi f_0\left(t-\frac{x_1}{v_l}\right)\right)$$
- ***Wavelength***:$$\lambda_w = {v_l \over f_0}$$
- ***Graph***:<br>![[Pasted image 20230719131639 1 1.png|333]]
- ***Real World Measures***:
	- ***Air***: $v_l \sim 340 \, {\text{m} \over \text{s}}$, $f_{\text{RANGE}} \in \left[50 \ \text{HKz} \div 1 \ \text{MKz}\right]$, $\lambda_w \in \left[7 \ \text{mm} \div 340 \ \mu\text{m}\right]$.
	- ***Water***: $v_l \sim 1500 \, {\text{m} \over \text{s}}$, $f_{\text{RANGE}} \in \left[1 \ \text{MKz} \div 10 \ \text{MKz}\right]$, $\lambda_w \in \left[1.5 \ \text{mm} \div 340 \ \mu\text{m}\right]$.
	- ***Steel***: $v_l \sim 6000 \, {\text{m} \over \text{s}}$, $f_{\text{RANGE}} \in \left[1 \ \text{MKz} \div 50 \ \text{MKz}\right]$, $\lambda_w \in \left[6 \ \text{mm} \div 1.2 \ \text{mm}\right]$.

---
###### [[SaM - Reflection of an Ultrasonic Wave]]
- ***[[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|Acustic impedance]]***:  $$Z = \rho \cdot v_l$$
- ***Reflection***:<br>![[Pasted image 20230925185349.png|500]]
- ***We define***:$$\begin{array}{l} v_i & \textit{(intial velocity of the wave)} \\[3px] v_{\tiny R} = \Gamma_{\tiny V} \cdot v_i & \textit{(velocity of the reflected wave)}  \\[3px] v_{\tiny T} = T_{\tiny V} \cdot v_i  & \textit{(velocity of the transmitted wave)} \\[3px] T_{11_i}  & \textit{(intial stress over the i-th dimension)} \\[3px] T_{11_{R}} = \Gamma_{\tiny T} \cdot T_{11_i} & \textit{(reflected wave's stress)} \\[3px]  T_{11_{T}} = T_{\tiny T} \cdot T_{11_i}   & \textit{(transmitted wave's stress)} \end{array}$$
- ***Formulas***:$$\begin{array}{l} T_{\tiny V} = {\huge{2 Z_1\over Z_1 + Z_2}}  & \textit{(transmitted coefficent for the velocity)} \\[7px] 
T_{\tiny T}  =  {\huge{Z_1-Z_2\over Z_1 + Z_2}}  & \textit{(transmitted coefficent for the stress)} \\[7px] 
\Gamma_{\tiny V}  = {\huge{2 Z_2\over Z_1 + Z_2}}   & \textit{(reflected coefficent for the velocity)} \\[7px] 
\Gamma{\tiny T}  =  {\huge{Z_2-Z_1\over Z_1 + Z_2}}  & \textit{(reflected coefficent for the stress)}
\end{array}$$
- ***Tilted reflection***:<br>![[Pasted image 20230720162211.png|500]]
- ***Formula***:$$\begin{array}{l}  \theta_2 = \theta_1  \\[3px]  {\large{\frac{\sin \theta_3}{Z_2} = \frac{\sin \theta_1}{Z_1}}} \end{array}$$

---
###### [[SaM - Scattering and Diffuse Reflection of an Ultrasonic Wave]]
- ***Scattering (if $D \ll \lambda_w$)***:<br>![[Pasted image 20230720162228.png|500]]
- ***Diffuse reflection (if $D \gg \lambda_w$, but the incident plane is not smooth)***:<br>![[Pasted image 20230925191317.png|500]]
- ***Terminology***:
	- $D$ : diameter of the obstacle.
	- $\lambda_w$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wavelength]].

---
###### [[SaM - Matching Layer for Acustic Impedance]]
- ***Before applying the matching layer***:
	- $Z_{{\text{PZT}}} = 32.5 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$.
	- $Z_{{\text{?}}} = 430 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$.
- ***Resulting [[SaM - Reflection of an Ultrasonic Wave|transmitted wave]] (pre-mathcing layer)***:$${v_{\tiny T} \over v_i} = {2 Z_{\text{PZT}}\over Z_{\text{PZT}} + Z_{\text{?}}}$$
- ***Strucutre***:<br>![[Pasted image 20230720162251 1 1.png|333]]
- ***Resulting [[SaM - Reflection of an Ultrasonic Wave|transmitted wave]] (post-mathcing layer)***:$${v_{\tiny T} \over v_i} = {2 Z_{\text{PZT}}\over Z_{\text{PZT}} + Z_{\text{A}}} \cdot {2 Z_{\text{A}}\over Z_{\text{A}} + Z_{\text{?}}}$$
- ***Real world values***:
	- $Z_{{\text{PZT}}} = 32.5 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$.
	- $Z_{{\text{?}}} = 430 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$.
	- _~Ex.: matching layer_ : $Z_A = 200 \ {\text{Rayl}}$.
		- After adding the mathcing layer, the ratio $\left({v_T \over v_i}\right)$ becomes $126.33\%$ of the intial value, so we have increased it.
	- As a rule of thumb we can consider a single acustic impedance that incorporates the material+matching layer: $Z_M = \sqrt{Z_{\text{A}} \kern2px Z_{\text{PZT}} \kern3px }$.
	- Given the thickness of the *PZT* layer: suppose $t_{\text{PZT}} = {\lambda_{\omega} \over 2}$, we usually take the thickness of the matching layer as $t_A = {\lambda_{\omega} \over 4}$. #NOT_SURE_ABOUT_THIS 
- ***Terminology***:
	- The unit of measure ${\text{kg} \over \text{m}^2 \kern2px \text{s}}$ is called a $\text{Rayl}$. 

---
###### [[SaM - Standing Waves]]
- _The reason [[SaM - Ultrasonic Transducers (Piezoelectric Device)|ultrasonic transducer]] vibrates is beacuse a **standing wave** resonates inside of the piezoelectric cristal_.
- ***Standing wave***:<br>![[Pasted image 20230720162328 1.png|500]]
- ***Formula***:$$\begin{array}{l} U & = & U_F+U_B \\[3px] & = & A \sin\left(2\pi{\large{x_1 \over \lambda_w}}-\omega t\right) + A \sin\left(2\pi{\large{x_1 \over \lambda_w}}+\omega t\right)      \end{array}$$
- _Real world example of a **standing wave**_:<br>![[Pasted image 20230925195247.png|500]]

---
###### [[SaM ~ Real World Example • Propagation of an Ultrasonic Wave in Different Materials]]
- ***Higher frequency***: _more **special resolution** (clearer images) but less **penetration depth**_.
- ***Real World Measures***:
	- ***Air***: $f \lt 1 \ \text{MHz}$, usually: $f \in [30 \ \text{KHz} \div 50 \ \text{KHz}]$.
	- ***Liquids (biomedical field)***: $f \in [1 \ \text{MHz} \div 10 \ \text{MHz}]$.
	- ***Solids (NDT - Non Destructive Testing)***: $f \in [1 \ \text{MHz} \div 50 \ \text{MHz}]$.
