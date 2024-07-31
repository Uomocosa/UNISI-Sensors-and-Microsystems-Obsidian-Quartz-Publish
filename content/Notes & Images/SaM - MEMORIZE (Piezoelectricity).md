##### List of things to memorize:
![[SaM - Piezoelectricity]]

---
###### [[SaM - Piezoelectric Effect]]
- ***Piezoelectric effect formula***:$$\left\{\begin{array}{l} \vec{D} = \overline{\overline{\varepsilon^{\tiny T}}} \vec{E} + \overline{\overline{d}} \kern2px \overline{\overline{T}} & \text{(direct piezoelectric effect)} \\ \overline{\overline{S}} = \overline{\overline{s}} \kern2px \overline{\overline{T}} + \overline{\overline{d^{\tiny T}}} \vec{E} & \text{(inverse piezoelectric effect)} \end{array}\right.$$
- ***Terminology***:
- $\vec D$, $\overline{\overline{\varepsilon}}$, $\vec E$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|displacement of the electric field, electric permittitivity matrix, electric field]].
- $\overline{\overline{T}}$, $\overline{\overline{S}}$ : [[SaM - Stress and Strain • Strain and Stress|stres and strain]]
- $\overline{\overline{d}}$ : [[SaM - Piezoelectric Coefficient Matrix for PZT|piezoelectric coefficient matrix]].
- $\overline{\overline{s}}$ : inverse piezoelectric coefficient matrix, or [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|yieldness coefficient matrix]].

---
###### [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect]]
- ***Piezoelectric effect formula***:$$\left\{\begin{array}{l} \vec{D} = \overline{\overline{\varepsilon^{\tiny T}}} \vec{E} + \overline{\overline{d}} \kern2px \overline{\overline{T}} & \text{(direct piezoelectric effect)} \\ \overline{\overline{S}} = \overline{\overline{s}} \kern2px \overline{\overline{T}} + \overline{\overline{d^{\tiny T}}} \vec{E} & \text{(inverse piezoelectric effect)} \end{array}\right.$$_Inverse piezoelectric effect_ : even if there is no stress applied to a piezoelectric material, but it is present an external electrical field ⇒ then we will see a deformation, or strain of the material itself.
- ***Different material with piezoelectric property***:
	- Quartz $(Si O_2)$ : _small losses_, almost a [[SaM - Complex Electric Permittivity|perfect dielectic]], $\varepsilon_r' \in [4 \div 5]$, $\varepsilon_r'' = 0.001$.
	- PZT (_Lead Zirconate Titanate_, _polycrystal_) : _large piezo-coefficients_ $(d_{33} = 500 \ {\text{pC} \over \text{N}})$
	- PVDF (_polymer_) : _low cost_
- ***Acutally***: #NOT_SURE_ABOUT_THIS (this is my reasoning)
	- The ***quartz*** has: $\varepsilon_r' \approx 4.0,\ \varepsilon_r'' =  0.001$ and $d_{12} \approx 2 \ {\text{pC} \over \text{N}}$.
	- The ***PZT*** has: $\varepsilon_r' \in [500\div 2000],\ \varepsilon_r'' \in  [0.01 \div 0.05]$ and $d_{12} \approx 500 \ {\text{pC} \over \text{N}}$.
	- Their [[SaM - Complex Electric Permittivity|complex electric permettivity ratio]] is almost the same ${\varepsilon_r' \over \varepsilon_r''} \sim 10^{-3}$ but the ***PZT*** has higher $d$ value, meaning if we take into the direct and inverse piezoelectric effect formual, it will result in a higer response given the same electric field $E$ and the same stress value $T$.<br>The same is true for the capacitance value $C_E = \varepsilon {A \over h}$ and charge output $Q = d \cdot F$, the PZT will have higher value for both.<br>==So for "raw performance" the **PZT** is better==.
	- However we have studied how we can vary some characteristics of the quartz, if we [[SaM - Types of Cut Quartzes|cut it in a different way]].<br>Also we have seen how the [[SaM - AT-Cut Quartz|AT-cut quartz]] has a linear relationship between its thickness $(t)$ and the wavelength $(\lambda_{\omega})$: $t \approx {\lambda_{\omega} \over 2}$.<br>==So the quartz give us "more flexibility"==.

---
###### [[SaM - Complete Piezoelectric Device (Actuator + Sensor)]]
- ***Actuator structure***:<br>![[Pasted image 20230719124208 1.png|333]]
	- A slice of piezo-material in between of two slices of conductive material, ==like a capacitance==.
- ***Direct piezoelectric effect formula with no external mechanical forces***:$$\overline{\overline{S}} = \overline{\overline{d}} \vec{E}$$
- ***Sensor structure***:<br>![[Pasted image 20230719124242 1.png|333]]
	- Acts again as a capacitance.
- ***Charge enclosed in the volume of the sensor***:$$Q = d\cdot F$$
- ***Equivalent lumped parameter system of the sensor***:<br>![[Pasted image 20230719124334.png|500]]
- ***Complete equivalent lumped parameter system***:![[Pasted image 20230924124545.png|500]]
- ***Different material with piezoelectric property***:
	- Quartz $(Si O_2)$ : _small losses_, almost a [[SaM - Complex Electric Permittivity|perfect dielectic]], $\varepsilon_r' \in [4 \div 5]$, $\varepsilon_r'' = 0.001$.
	- PZT (_Lead Zirconate Titanate_, _polycrystal_) : _large piezo-coefficients_ $(d_{33} = 500 \ {\text{pC} \over \text{N}})$
	- PVDF (_polymer_) : _low cost_

- ***Terminology***:
	- $\overline{\overline{d}}$, $d$ : [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficient]].
	- $F = k \cdot x$ : force, elastic coefficient and displacement.


---
###### [[SaM - Compact Piezoelectric Coefficient Matrix for PZT • Dependence of Piezoelectricity on Temperature • Curie Temperature]]
- ***Piezoelectric coefficient matrix in compact notation for PZT***:$$\overline{\overline{d}}_{\text{PZT}} = \left[\begin{array}{l} 0 & 0 & 0 & 0 & d_{15} & 0 \\ 0 & 0 & 0 & d_{24} & 0 & 0 \\ d_{31} & d_{32} & d_{33} &  0 & 0 & 0 \end{array}\right]$$
- ==_Piezoelectric materials have to be operated under the Curie temperature_==.
- **Curie Temperature**: _is the temperature at which, usually, there is a phase transition from an asymmetrical to a symmetrical crystal_.
- For ***PZT*** this temperature is $T_C = 250°\text{C}$.

---
###### [[SaM - Piezoelectric Accelerometer]]
- ***Structure***:<br>![[Pasted image 20230719130505.png|500]]
- ***Equivalent Circuit***:<br>![[Pasted image 20230924180117 1.png|500]]
- ***Output formula***:$$V(s) = {s\kern1px R_T \kern2px k \kern2px d  \over 1 + s \kern1px R_T C_T}\cdot H(s)\cdot a(s)$$
- ***Terminology***:
	- $\omega_n$ : natural frequency $\left(\omega_n \simeq \omega_0 = \sqrt{k \over m_s}\right)$
		- $k$ is the spring consntant of our accelerometer, and $m_s$ the sismic mass.
	- $C_T = C_E + C_L$
	- $R_T = R_L \parallel R_A \approx R_L$
	- ==$C_L$ and $R_L$ depend on the **wire's lenght** (bad)==.
	- $a(s)$ : laplace transform of the acceleration $a(t)$.
	- $H(s)$ : [[SaM - Accelerometer|accelerometer's transient function]] $\left(H(s) = {\huge\frac{m_{\tiny{S}}}{k} \frac{1}{{m_{\tiny{S}} \over k}s^2 + {\lambda \over k}s + 1}}\right)$
- ***Bode Plot***:<br>![[Pasted image 20230719130633.png|500]]<br>![[Pasted image 20230719130657.png|500]]
- ***Frequency range***:$$f \in \left[{10 \over R_T C_T},\ {\omega_n\over 10}\right]$$
- _The overall system is [[SaM - AC-Coupled Amplifier|AC-coupled]]. ⇒ ==You cannot sense **static** acelerations==_.
- ***Lower cutoff frequency***: #NOT_SURE_ABOUT_THIS <br>The professor wrote $f_L = {1 \over 2 \pi C_T R_L}$<br>This is probably wrong, since we have already defined $f_L = {10 \over C_T R_L}$
- ***Constant sensitivity inside the frequency range***:$$\alpha = {V(\omega) \over a(\omega)} = {m_s \cdot d \over C_T}$$
- ***Problem***: _the sensitivity depends the capacitance $C_T$, wich depends on the **cable capacitance**_.<br>***Solution***: _make the amplifier (read-out electronics) a part of the sensor itself_:<br>![[Pasted image 20230719130803.png|500]]
	- _This particular kind of piezo-accelerometer are called **IEPE** or **ICP**_.


---
###### [[SaM - Ultrasonic Transducers (Piezoelectric Device)]]
- ***Structure***:<br>![[Pasted image 20230719131157 1.png|500]]
- ***Structure***:
	- A [[SaM - Piezoelectric Effect|piezoelectric]] slice of material (like [[SaM - Quartz Oscillator|quartz]]).
	- An added dumper $\lambda$.
	- A source voltage for exiting the piezoelectric.
	- A read-out (an amplifier) to read the output from the piezolectric.
- ***Workings***:
	1. We exite the piezoelectric, which is deformed [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|inverse piezoelectric effect]], and we make it vibrate.
	2. The vibration generates a [[SaM - Ultrasonic Waves|wave]].
	3. The wave bounces off the **target**, and returns to the piezoelectric, make it vibrate again.
	4. We measure the new vibration with the read-out.
- ***$V_g$ and output graph***:<br>![[Pasted image 20230925111343.png|500]]
- ***Electrical circuit for actuator and sensor***:<br>(_This is a [[SaM - Coarse Approximation of the Lumped Parameter Model of an Ultrasonic Transducer|coarse approximation]]_)<br>![[Pasted image 20230719131223.png|500]]
	- _The two diodes are a **protection circuit**, for read-out part, ==it protects the amplifier when using the device as a transducer==_.
- ***Used as an actuator (both diodes are ON)***:<br>![[Pasted image 20230719131247 1.png|500]]
	- ***Output graph of $\dot x(t)$***<br>![[Pasted image 20231214122558.png|333]]
	- ***Relative output $\left(\left|{\dot x(\omega) \over V}\right|\right)$ graph***:<br>![[Pasted image 20230925112924.png|500]]
- ***Used as a sensor (both diodes are OFF)***:<br>![[Pasted image 20230719131256.png|500]]
	- ***Output charge formula***:$$Q_p = k \kern2px d \kern2px x$$
	- ***Transfer function***:$${V \over F_{ext}} = {R_p \kern2px d \over 1 + j \omega R_p C_p} \kern2px H_u(\omega)$$Where:$$H_u(s = j\omega) = \frac{s}{\frac{m}{K}s^2 + \frac{\lambda}{K}s + 1}$$Please note the difference with the transfer function $H(s)$ of the [[SaM - Accelerometer|acceleroemeter]], do not confuse them.
	- ***Plot of $H_u$ and ${R_p \kern2px d \over 1 + j \omega R_p C_p}$, the complete output graph is their multiplication***:<br>(This device should be excited with a frequency $f\approx {\omega_{\kern-2px\tiny N} \over 2 \pi}$)<br>![[Pasted image 20230719131324 1.png|500]]

---
###### [[SaM - Coarse Approximation of the Lumped Parameter Model of an Ultrasonic Transducer]]
- "_The lumped parameter approximation of this device is an **extreamely coarse approximation**, since the the **wavelenght** $\lambda_w$ is NOT larger than the **dimension of the crystal** ($h$)_".
- So $\lambda_{w} \ngtr h$ ⇒ **coarse approximation**.

---
###### [[SaM - Quartz Oscillator]]
- ***Lumped parameter system***:<br>![[Pasted image 20230720165950 1.png|500]]
- ***[[SaM - AT-Cut Quartz|Wavelenght-thickness real world relationship]]***:$$t \approx {\lambda_w \over 2}$$
- ***AT-cut quartz as a sensor, equivalent electrical circuit***:<br>![[Pasted image 20230720170012 1.png|500]]
	- ***Formulas***:$$\begin{array}{l}   L_{eq} = {\large{m \over k^2 d^2}}  \\[2px]  R_{eq} = {\large{\lambda \over k^2 d^2}}  \\[4px]  C_{eq} = kd^2 \end{array}$$
	- ***If we want to consider the added "mechanical impedance of the medium"***:$$Z_M \over k^2 d^2$$_==Usually negligible==_.
	- _The piezoelectric behavior of this structure depends on the surface orientation with respect to the [[SaM - Crystallographic Axis|crystallographic axis]]_.
- ***Terminology***:
	- $m,\ \lambda,\ k$ : mass, dumping coefficient, elastic coefficient of the [[SaM - Piezoelectric Effect|piezoelectric]] slice.
	- $d$ is the [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficient]].
	- $Z_M$ : **mechanical impedance of the medium**, as an example when we talked about the [[SaM - Ultrasonic Transducers (Piezoelectric Device)|ultrasonic transducer]] we said that it used an "added damper", in that case $Z_M$ would represent this added dumper.

---
###### [[SaM - AT-Cut Quartz]]
- ***Lumped parameter system***:<br>![[Pasted image 20230720170030 1.png|500]]
- ***Real world values for $\omega = 10 \ \text{MHz}$***:$$\begin{array}{l}   L_{eq} = 100 \ \text{mH}  \\[2px]  C_{eq} = 15 \ \text{fF}  \\[4px]  R_{eq} = 20 \ohm \end{array}$$_**Remember**: $1 f = 10^{-15}$_.
- ***Reactance $X_{eq}$, given: $R_{eq} = 0$ and $Z_{eq} = j X_{eq}$***:$$X(\omega) = - {{1- \omega^2 L_{eq} C_{eq} \over 1 - \omega^2 L_{eq} {\large {C_E \kern2px C_{eq} \over C_E + C_{eq}}}}}$$
- ***If we consider that $C_E \ll C_{eq}$, and low frequencies***:$$X(\omega) = -{1 \over \omega  \kern2px C_{\kern-2pxE}}$$
- ***Frequencies to remember***:$$\begin{array}{l} \omega_s = {\huge\sqrt{{1 \over L_{eq} \kern1px C_{eq}}}}  \\[3px] \omega_p = {\huge\sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq} \kern1px C_{eq}}}}    \end{array}$$
- _We have also seen the previous formula written as_:$$X_{eq} = - {1\over\omega C_{\kern-2pxE}}{1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$$
- ***Plot of ${1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$***:<br>![[Pasted image 20230720170319 1.png|500]]
- ***Plot of $X_{eq}$***:<br>![[Pasted image 20230720170111 1.png|500]]
- ==_There is a really small range in which the quartz acts as an inductance_==.<br>==_Moreover this range is set by the **physical** properties of the quartz, that define $\omega_s$ and $\omega_p$_==.
- ***Wavelenght-thickness real world relationship***:$$t \approx {\lambda_w \over 2}$$
- ***Plot if $R_{eq} = 0$***:<br>![[Pasted image 20230926190017.png|333]]
- ***Plot if $R_{eq} \neq 0$***:<br>![[Pasted image 20230720170218.png|333]]
- ***Real world measures***:
	- The percentage difference (calculated like a relative error) of $\omega_s$ and $\omega_p$ is $10^{-5} \, \%$, (really small difference between $\omega_s$ and $\omega_p$).
	- So let's take for example $\omega_s = 10 \ \text{MHz} = 10{\small^{'}}000{\small^{'}}000 \ \text{Hz}$ then $\omega_p = 10{\small^{'}}000{\small^{'}}100 \ \text{Hz}$.

---
![[SaM - MEMORIZE (Piezoresisitivity)#SaM - Crystallographic Axis]]

---
###### [[SaM - Types of Cut Quartzes]]
- _The way we cut the quartz, will relfect how it works_:<br>![[Pasted image 20230720170252.png]]
- _==Cut-Quartzes work in in **frequency up to $30$ MHz**==.<br>==The "***thickness shear mode***" has the highest frequency range==_.
- _This frequency changes with temperature, and all cuts have a slope around $T_A$ (ambience temperature)_:<br>![[Pasted image 20230720170305.png|333]]

---
![[SaM - MEMORIZE (Oscillators)#SaM - Quartz in a 3 Point Oscillator]]
######
###### [[SaM - Behavior of the Quartz Ocillator at High Frequencies]]
- ***[[SaM - AT-Cut Quartz|AT-cut quartz's impedance]]***:$$Z_{eq} = C_E \parallel (L_{eq} + R_{eq} + C_{eq})$$
- ***[[SaM - AT-Cut Quartz|Real world values of an AT-cut quartz]] for $\omega = 10 \ \text{MHz}$***:$$\begin{array}{l}   L_{eq} = 100 \ \text{mH}  \\[2px]  C_{eq} = 15 \ \text{fF}  \\[4px]  R_{eq} = 20 \ohm \end{array}$$_**Remember**: $1 f = 10^{-15}$_.
- ***[[SaM - AT-Cut Quartz|AT-cut quartz special frequencies]]***:$$\begin{array}{l} \omega_s = {\huge\sqrt{{1 \over L_{eq} \kern1px C_{eq}}}}  \\[3px] \omega_p = {\huge\sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq} \kern1px C_{eq}}}}    \end{array}$$
- ***[[SaM - AT-Cut Quartz|AT-cut quartz reactance formula]]***:$$X_{eq} = - {1\over\omega C_{\kern-2pxE}}{1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$$
- ***Plot of ${1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$***:<br>![[Pasted image 20230720170319 1.png|500]]
- ***More precise equivalent system for an AT-cut quartz at high frequencies***:<br>![[Pasted image 20230720170338 1.png|500]]
	- _Instead of_:<br>![[Pasted image 20230720170030 1.png|333]]
- ***Additional components formulas***:$$\begin{array}{l}   L_{m_i} = {1 \over 8}{m \over k^2 d^2}  \\[5px]  C_{m_i} = {8 \over (i \cdot \pi)^2}k d^2  \\[4px]  R_{m_i} = {(i \cdot \pi)^2 \over 8}{\lambda \over k^2 d^2} \end{array}$$And:$$\omega_{s_i} \approx i \cdot w_{s_1}$$Where: $i = 1,\ 2 ,\ \ldots$
- ***Real world measure***:
	- "_Low frequency_", in this case means: $\lt 10 \ \text{MHz}$.
	- "_High frequency_", in this case means: $[20 \ \text{MHz} \div 30 \ \text{MHz}]$, or more.

---
###### [[SaM - Quartz as a Sensor • QCM (Quartz Crystal Microbalance)]]
- ***Structure and equivalent system***:<br>![[Pasted image 20230720170400.png|500]]
- _The name of this sensor is: **QCM** (*Quartz Crystal Microbalance*)_.<br>_==It is based on the concentration of the target species (that gets absorbed by the functionalization layer)==_.
- ***Functionalization layer impedance formula***:$$Z_{M} = \Delta m \kern15px \Rightarrow \kern15px  {Z_{M}\over k^2 d} ={\Delta m\over k^2 d}$$
- ***Changes to the equivalent components of this sensor, with respect to the normal [[SaM - AT-Cut Quartz|AT-cut quartz]]***:$$L_{eq}' = L_{eq} + {\frac{\Delta m}{K^2 d}} \kern15px\Rightarrow\kern15px \left\{\begin{array}{l} \omega_s' = {\huge{1 \over {\sqrt{L_{eq}' \cdot C_{eq}}}}}   \\[5px] \omega_p' = {\huge\sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq}' \kern1px C_{eq}}}}  \end{array}\right.$$
- ***Terminology***:
	- $\Delta m$: mass of the "***functionalization layer***"
	- $K$ : cosntant defined by the geometry of the piezoelectric crystal
	- $d$ : [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficients]].
	- $L_{eq} = {m \over k^2 d^2}$ defined [[SaM - Quartz Oscillator|previously]].

---
