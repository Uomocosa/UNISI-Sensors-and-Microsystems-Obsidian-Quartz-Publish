##### List of things to memorize:
![[SaM - Inductive Sensors]]

---
###### [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance]]
- _They usually give a **very large output signal**_.
- _They are also **robust**_.
- ***Lumped parameter***:
	- **Effort quantity**: $\text{MMF}$ (*Magneto Motive Force*) $\left[\text{A}\cdot\text{turn}\right]$ (**ampere** $\cdot$ **turns**, since it is found multipling the current per the number of turns of a inductance).
	- **Flow quantity**: $\phi(B)$ *(Flux of the Magnetic Field)* $\left[V \cdot s\right]$ (**volt** $\cdot$ **seconds**).
	- ***Basic structure of a magnetic circuit***:<br>![[Pasted image 20230719112102.png|500]]
	- ***Magnetic field lines, and powered coil***<br>![[Pasted image 20230719112119.png|500]]
	- ***Lumped parameter system, with no PM***:<br>![[Pasted image 20230719112153 1.png|500]]
	- ***Formulas***:$$\begin{array}{l}  \mathcal{R}_g = \large{l_g \over \mu_0 S_g}  \\[3px]  \mathcal{R}_c = \large{l \over \mu_{\small{C}} S_C}  \\[3px]  \phi(B) = \normalsize{\mu_0 \kern2px H_g S_g} = \normalsize{\mu_{\small{C}} \kern2px H_C S_C}  \end{array}$$
	- ***Lumped parameter system of the powered coil***<br>![[Pasted image 20230719112222.png|500]]
	- ***Formulas***:$$\begin{array}{l}  \mathcal{R}_M = \large{l_M \over \mu_M S_M}  \\[3px]  \text{MMF} = \mathcal{R}_M \cdot \phi(B_r)  \\[3px]  \phi(B_r) = S_M \cdot B_r = \mu_0 \cdot S_M \cdot M_r  \end{array}$$
	- ***Complete lumped parameter system***:<br>![[Pasted image 20230719112237 1.png|500]]
	- ***Electro-motive force formula***:$$\begin{array}{l} v &=& -N{\huge{d\phi(B) \over dt}} \\[7px] &=&  -{\huge\frac{N^2}{\mathcal{R}_{TOT}}\frac{dI}{dt}} + \left({\huge\frac{N^2}{\mathcal{R}_{TOT}^2}}I+{\huge\frac{N}{\mathcal{R}_{TOT}^2}}\text{MMF}_{eq}\right){\huge\frac{d\mathcal{R}_{TOT}}{dt}}    \end{array}$$
	- ***Terminology***:
		- $l_g$: length of the gap.<br>(_The pedix $_g$ will always refer to the gap_)
		- **PM**: Permament Magnet.<br>(_The pedix $_M$ will always refer to the permamanent magnet_)
		- $S_C$ : surface of the core.<br>(_The pedix $_C$ will always refer to the core_)
		- $\mu_{\small{C}} = \mu_0 \kern2px \mu_r$ ([[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|permeability]] of the core).
		- $H$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field intensity]] $(\mu \cdot H = B)$.
		- $\mu_M = \mu_0 \kern2px \mu_{\text{magnet}}$.
		- $M$ is the **[[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetization]]** $(M = H \cdot \mathcal{X}_M)$
		- $\mathcal{X}_M = 1 + \mu_r$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic susceptibility]].


---
###### [[SaM - VRS (Variable Reluctance Sensors)]]
- ***Basic strucuture for an active VRS***:<br>![[Pasted image 20230719112428 1.png|333]]
- ***Formula***:$$v = N {\text{MMF}_{eq} \over \mathcal{R}^2_{TOT}}{d \mathcal{R}_{TOT} \over d t}$$
- ***Example for a speed VRSensor***:<br>![[Pasted image 20240215181018.png|333]]
- ***Its lumped parameter system***<br>![[Pasted image 20240215181103 1.png|333]]
- ***Formula***:$$v \approx N {\text{MMF}_{eq} \over \mathcal{R}^2_{TOT}}\cdot \alpha {dx \over dt}$$**NOTE**: $\mathcal{R}_{TOT}$ depends on $\mathcal{R}_{gap}$ which changes, it is NOT a linear sensor.
- ***Plot***:<br>![[Pasted image 20240215181138.png|500]]
- **Period**:$$T = {1\over \omega \cdot \#{\text{theeths}}}$$***N.B.***: the amplitude of the graph will scale with $\omega$, not just the period.<br>_This can be a problem, because we will have a good **signal to noise ratio** (**SNR**) when the machine is rotating fast, and a lower one when it rotates slow_.<br>==_If the machine is still the only thing I will measure will be the noise_==.
- ***Terminology***:
	- $v$ is the [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|electro-motive force]] (==this is actual voltage measured in Volts, but has sign inverted with rispect to the actual voltage drop==).
	- $\text{MMF}_{eq}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|equivalent magneto motive force]].
	- $\mathcal{R}_{TOT}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|total reluctance]]
	- $\alpha$ : non-specified constant. NOT the sensitivity.
	- $\omega$ (previously called $\omega_M$) is the **angular velocity**.
	- $\#{\text{theeths}}$ : number of theets.

---
###### [[SaM - Eddy Currents • Eddy Probe]]
- ***Conductive, non-ferromagnetic $(\mu_T \simeq \mu_0)$ target, with a coil exited with Alternated Current (AC)***:<br>(_In order to have a "measurable eddy current effect", usually we use **very high frequency** $\sim 2 \text{MHz}$_)<br>![[Pasted image 20230719112556.png|500]]
- _The "Eddy current", forms a magnetic field which **opposes to the variation of the flux**_.
- _Eddy currents probe can be used, but ==they need to be calibrated depending on the material== (**not good**)_.
- ***Minum skin depth***:$$t \gt \delta = \frac{1}{\sqrt{\pi \sigma f \mu_T}}$$
- ***Electrical equivalent cirucuit***:<br>![[Pasted image 20230719112630.png]]
- ***Impedance formula***:<br>(*NOT IMPORTANT, too difficult*)$$Z = \underbrace{R_1 + {\omega^2 M(x) R_2 \over R^2 + \omega^2L_2^2}}_{\huge R_e} + j\omega \kern0px \underbrace{\left(L_1 - {\omega^2 M(x) L_2 \over R_2^2 + \omega^2L_2^2}\right)}_{\huge L_e}$$
- ***Simplified formula***:$$Z \triangleq {v \over i_1} = R_e + j\omega L_e $$
- ***Real World Measures***:
	-  **Skin depth** $(t)$ of various material, with $f = 1 \ \text{MHz}$:
		- *Alluminum*: $\delta = 84 \ \mu m$
		- *Permalloy*: $\delta = 2 \ \mu m$
		- *Steel*: $\delta \in [ 12 \ \mu m \div 400 \ \mu m ]$
	- ***Equivalent percentage inductance $L_e(x) \over L_0$, with different materials***:
		- Some materials increases their inductance $L_e(x)$, like *Stell*.
		- While other decreases their inductance, like for example *Alluminum*.
		- Also the percentange change of $L_e(x) \over L_0$ can assume values of around $[\sim 80\% \div 120\%]$.
		- Graph:<br>![[Pasted image 20230719112730.png|333]]
- ***Terminology***:
	- $t$ : thickness.
	- $\delta$ : penetration depth of the magnetic field.
	- $\sigma$ :  the **conductivity** of the target.
	- $f$ : frequency of the excitation.
	- $\mu_T$ : permittivity of the target.
	- $M(x)$ : [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction|magnetic induction]]
---
###### [[SaM - Front End for an Eddy Probe]]
- This circuit uses an [[SaM - Eddy Currents • Eddy Probe|Eddy Probe]], to represent it I use the symbol of the inductance with 2 lines in front ($Z_2$):<br>![[immagine_2023-09-21_160434259-transformed 1.png|500]]
- We need a [[SaM - Carrier Amplifier|carrier amplifier]], a **synchronous demodulator**, and a [[SaM - Logarithmic Amplifier|logarithmic amplifier]].
- In this case, there is another probe ($Z_1$), which is not exposed to the target, it's not facing the target, and it's in an **enclosed** situation.<br>==It is used only to compensate the temperature effect on the actual sensor==, since the coil and also the resistance are sensitive to temperature.

---
###### [[SaM - Different Solutions for Contactless Probes • Inductive Senors vs. Capacitive Sensors]]
1. ***Mechanical Load***:<br>==Using common values the force exrted by a ***CAPACITANCE*** probe (using common values for $V$, $I$ and all other parameters) is $100$ times less than than that need by inductance probe==, so usually: $F_C \ll F_L$<br>Capacitive load: $F_C = -\frac{1}{2}\frac{\varepsilon A}{x^2}V^2 = \frac{1}{2}\frac{CV^2}{x}$<br>Inductive load: $F_L = \frac{1}{2}\frac{N^2 \mu_0 A_g}{x}I^2 = \frac{1}{2}\frac{LI^2}{x}$
2. ***Range of Measurement***:<br>For **inductances** ([[SaM - Eddy Currents • Eddy Probe|Eddy current]]), we can speak about a ratio of $1:3$, which refers to **range** with respect to **probe diameter**.<br>For [[SaM - Capacitive Proximity Sensors|capacitances]], instead, we have a $1:8$ **range/diameter** ratio.<br>⇒ ==So the longer range is obtained with ***INDUCTIVE*** solutions==.
3. ***Spatial Resolution***:<br>What I sense is an **average** of the distance over a certain area, this area is called "**the spot**".<br>For **inductive** sensors the ratio between **the spot diameter** and **the probe diameter** is $1.3:1$.<br>While for **capacitive** sensors it is $3 : 1$.<br>⇒ ==So if we want to measure the avarage distance in a large area we may opt for an ***INDUCTIVE*** solution, instead if our target is small we may opt for a **CAPACITIVE** one==. 
4. ***Complexity of Front End***:<br>==For **capacitive** sensor, the front end is **far more complex**==.<br>In fact, the **INDUCTIVE probe gies large signals that don't need particular care for** conditioning, for noise and so on.
5. ***Complexity of the Probe Itself***:<br>==For **CAPACITIVE** sensor, the probe is just a plate, it is **far less complex** than the inductive probe==.<br>The only problem for capcitive proximity probes, is to ensure there is an **sufficient insulation** between the plate and the shield and so on, so this is the only problem. 
6. ***Environmental Conditions***:

| Eddy currents (_inductive sensors_)                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Capacitive** sensors                                                                                                                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| $\delta$: The target needs to have a minimum thickness.<br><br>Also there is some restriction on target's characteristic: $\mu$ (permeability) and $\sigma$ (conductivity).<br>The **uniformity of the material**, and the **surface type**.<br><br>The target has to be homogeneous in order to be able to use the calibration that we have done with that specific material.<br>⇒ If you change material type or if you have a non-homogeneous material, then you can find problems. | The target is not influential, the target is uniformity is not influential, same for the target's characteristics, surface roughness and so on, because **we only need the target is conductive**.                                                           |
| Then we have the possibility of having an **external magnetic field** which disrupts the measurement.                                                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                              |
| And finally **temperature**.                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Temperature is not influential**, unless you go to very high temperature, which can change the directly behavior of the air or the gas in between being to plate, but this is in extreme condition (when $\varepsilon$ becomes variable with temperature)  |
| Tho if I place *dirt*, *humidity*, ..., in between the probe tip and the target, if it has the same permittivity and is not conductive ⇒ **then it doesn't matter**.<br>==For this reason, **inductive** sensors are robust for **industrial applications**==                                                                                                                                                                                                                          | Instead it is influential: **dirt**, **oxidation of the plates**, because it's like placing the different direct there, **humidity** (sometimes) or condensed water (everytime), finally the **electrical field** is also influential for conductive sensors |

---
###### [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction]]
- ***Mutual inductance formula***:$$\begin{align}&V_1 = j\kern2px \omega \kern1px M \kern1px i_2\\&V_2 = j\kern2px \omega \kern1px M \kern1px i_1\end{align}$$
- ***LVDT sensor structure***:<br>![[Pasted image 20230719114148.png|333]]<br>![[Pasted image 20230719114202.png|333]]
- ***Electric circuit****:<br>![[Pasted image 20230719114229 1.png|500]]
- ***Output formula***:$$V_{out} = \frac{ j \omega R_Lk x E_1}{(R_1 + j\omega L_1)(R_2 + j\omega L_2)}$$
- ***Bode plot of the relative sensitivity***:<br>![[Pasted image 20230719114256.png|500]]
- ***Simplified formula, in the linear region***:<br>(*So:  $f_{exc} \in \left[f_1 ,\ f_2\right]$, $R_L \gg R_1,\ R_2',\ R_2''$ ⇒ $R_2 \gg R_1$ and $R_2 \approx R_L$*)<br>(*Like other sensors, this looses the sign of $x$*)$$\frac{kxR_L}{R_2L_1 + R_1 L_2} \simeq \frac{k}{L_1}|x|$$
- ***Commonly we select $f_{exc} \simeq f_0$, where***:$$f_0 = {1 \over 2\pi} \sqrt{{R_1 R_2 \over L_1 L_2}}$$
- ***Output graph***:<br>![[Pasted image 20230719114323.png|333]]
- ***Complete circuit, with sign-recovery***:<br>![[Pasted image 20230719114348.png|500]]
- ***Terminology***:
	- $M_1 - M_2 = kx$ (linear approximation).
	- $R_2 = R_2' + R_2'' + R_L$
	- $L_2 = L_2' + L_2''$
	- ==Remeber that this model is valid for $f_s \ll f_{exc}$==, meaning that the mesurand $x$ must vary relatevely slowly to the exatitaion, so that we can consider $x$ constant to respect to the exatation signal $E_1$.
	- We can approximate this sensor as linear if we stay in the "linear range" defined by $[-x_{LIN},\ +x_{LIN}]$.<br>But sometimes it is accepted to work in the **extended range**: $[-x_{MAX},\ +x_{MAX}]$.

---
###### [[SaM - 5 Wires LVDT (Linear Variable Differential Transformer)]]
- ***Circuit***:<br>(_By adding a wire the [[SaM - Carrier Amplifier|carrier amplifier]] for sign recovery, is no longer needed_)<br>![[Pasted image 20230719114407.png|500]]
- ***Formulas***:$$\begin{array}{l} M_1 = M_0(1+kx)  \\ M_2 = M_0(1-kx)    \end{array}$$So:
	- $kx$ this time is a little more complicated and it is defined as: $kx = {M_1 - M_2 \over 2 M_0}$<br>So: $M_1-M_2 = 2 M_0 k \kern2px x$
	- $M_0$ is the **mutual induction** of both $M_1$ and $M_2$ at rest.
- ***Output for $x=0$, $x\gt0$, $x\lt0$***:<br>![[Pasted image 20230719114430.png|500]]
- ***Complete circuit, with compensation for temperature $(T)$ and noise $(E)$***:<br>![[Pasted image 20230719114440.png|500]]

---
###### [[SaM - Hall Sensor]]
- ***Simple strucuture for the "Hall effect"***:<br>(_It must be a **conductive material**_)<br>![[Pasted image 20230719114550 1 1.png|333]]
- ***Lorentz force formula***:$$\vec F = q \kern2px \vec v \times \vec B$$
- ***More complex drawing, with angles***:<br>![[Pasted image 20230719114550 1.png|333]]
- ***Formula***:$$qvB\sin\theta=qE$$Where: $E = {V_H \over d}$, so:$$V_H = v B d \sin\theta$$
- ***Final formula***:$$V_H = BI\kern2px{K_H \over t}  \sin \theta$$
- ***Real World Masures***:
	- This device can be used to:
		1. **Sense a magnetic field** (if I know $I$).
		2. **As a displacement sensor** (if used with a **permament magnet**, so that I know $B$, and I also need to know $I$).
		3. **To measure the angle $\theta$** (I must know $I$, $B$).
		4. **Current sensor** (I must know $B$).
	- Advantages of an "_Hall sensor_":
		1. **Easily intefrated** (with read-out, current generator and temperature compensation).
		2. The whole package (with compensation) **can be sealed**.
		3. **Insensitive to contaminants in the enviroment**.
		4. **Simple structure**.
		5. Large ranges for magnetic fields $(B)$, and large bandwith $B_w = 100 \ \text{KHz}$.
		6. **Low cost device**.
- ***Terminology***:
	- $\vec B$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field]].
	- $t$ : thickness.
	- $d$ : width.
	- $l$ : lenght.
	- $I_B$ : current in a solenoid, used to generate $B$.
	- $I$ : current flowing in the conductive material.
	- $\vec v$ : velocity of the free charge moving due to the current $I$.
	- $E$ : potential.
	- $q = -1.602 \cdot 10^{-19} \ \text{C}$ charge of the electron.
	- $V_H$ : measured voltage across the conductive material.<br>Measured perpendicular to $I$.
	- $K_H \triangleq {\large{1 \over nq}}$ : "***Hall coefficient"***.
		- $n$ : [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|density of carriers]].
