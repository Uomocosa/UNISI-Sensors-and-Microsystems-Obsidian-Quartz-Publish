##### ***Remeber***:

> - A Metal Strain Gauge is a **passive sensor** that relates its own resistence value to the **deformation** or **strain** it's under.
> - Here we can see a scheme for a simple piece of **uniform**, **omogeneus**, **isotropic** bar of metal being used as a metal strain gauge:<br>![[Pasted image 20231127191427 1.png|333]]

> #IMPORTANTE 
> - To calculate the change in resistance due to strain, we can use the following formulas:
> 	1. [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|Basic resistance formula]]: ${R} = \rho {l \over S}$.
> 	2. [[SaM - Piezoresistivity Effect|Piezoresistivity effect for metal]]: ${d\rho \over \rho} = c {dV \over V}$.
> 	3. [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|Definition of stress]]: $\varepsilon = {\Delta x \over x}$.
> 	4. [[SaM - Young and Poisson Modulus|Poisson modulus]]: $\nu = {\varepsilon_{\perp} \over \varepsilon_{\parallel}}$.
> - And from them we obtain the percentage variation of resisitance of a strain gauge:$$R=R_0(1+G\varepsilon_x)$$Where:
> 	- This formula of strain gauge is really similar to [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen Equation for RTDs]].
> 	- It is important to note however that for strain gauge $G\varepsilon_x$ is at most in the order of $0.1$, (or $10\%$ variation) so the variation of resistance is really small.<br>Instead for the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 sensor]] (a particular [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensor]]) the variation of resistance can even be $\times4$ (or $300\%$ variation) of its initial value.
> 	- $\varepsilon_x$ is the strain along the $x$-axis (can also be called $\varepsilon_{\parallel}$).<br>Its max value for normal metal strain gauges, or [[SaM - Working Range & Safe Range|working range]] **does not exceed $50^{.}000 \mu \varepsilon$** ($\mu \varepsilon$: microstrain, $\mu \varepsilon=10^{-6}$).
> 	- $G$ is the **Gauge Factor**, it has values between $[2\div 4]$, and it is equal to:$$G=1+2\nu + c \kern3px (1-2\nu)$$Where:
> 		- $\nu$ is the **Possoin module**.
> 		- $c$ is the [[SaM - Piezoresistivity Effect|piezoresistive coefficient]].

> #IMPORTANTE 
> - This are some real world, standard values for metal strain gauges:<br>![[Pasted image 20231127192314 1.png]]
> - $R_0$ for the strain gauge can assume the values reported above, so between $[50\ohm \div 700\ohm]$.
> - It is important to choose a material that has **low [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|TCR]]** (*Temperature Coefficient of Resistance*), while we have seen for **RTDs** that the opposite is true.<br>The metals and alloy we choose for strain gauge have a TCR between $[10^{-5}°\text{C}^{-1} \div 10^{-6}°\text{C}^{-1}]$.

> A strain gauge has this structure:<br>![[Pasted image 20231128114747 1.png|333]]
> - In this way we can increase the "**parallel resistance**" $R_{\parallel}$, while keeping the "**perpendicular resistance**" $R_{\perp}$ to a low value.<br>==This kind of structure allows to have a **small transverse sensitivity**, which means we only sense displacement in the $x$ direction, and almost in the $y$ direction==.<br>==The sensitivity on the $y$ axis is $\lt 1\%\div 2\%$ with respect ot the sensitivity on the $x$ axis==.
> - However due to the "**Transverse Sensitivity**" created by the perpendicular resistance ($R_{\perp}$) we need to change the totatl resistance value, to account for this small change:$$R=R_0\left(1+G \kern2px \varepsilon_l + G_T \kern3px \varepsilon_T \right)$$Where: $G_T$ is the ***transverse gauge factor***.
> - For **uniaxial stresses** we can rewrite this formula as:$$R=R_0(1+G_v \cdot\varepsilon_x)$$Where:
> 	- $G_v = G_V= G-G_T\cdot\nu$ 
> 	- $\nu$ is the [[SaM - Young and Poisson Modulus|Poisson modulus]].
> - So the transverse stress can be seen as just a reduction of the **gauge factor**.

> Another change that could happen, resulting in an addition or subctraction to the total resistance value is the **Temperature Effect**, so due to the change in resisitivity of the metal, and the **thermal expansion** of both the "**metal grid or structure**" and the **substrate** (the thermal exapansion will create a strain), so we need to account for:
> ![[Pasted image 20231128121053.png]]
> - The TCR was first seen in the [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD lecture]].
> - The TCS will be ignored since too small.
> - For the Thermal exampansion we need to define two coeffieicents:
> 	- $\lambda_S$ : ***thermal exampsion coefficients of the substrate***.
> 	- $\lambda_{TO}$ : ***thermal exampsion coefficients of the metal grid or structure***.
> 
> So we have that, if we account for all possible changes to the resistance we obtain:$$R=R_0(1 + \alpha T + G \varepsilon_x + G \varepsilon_{TH} + G_T \varepsilon_{TH})$$Where:$$\varepsilon_{TH} = (\lambda_S - \lambda_{TO})\cdot \Delta T $$

> Here some other material:
> - [Youtube 'Strain Gauge 101 - Learn the basics of how they're used](https://www.youtube.com/watch?v=BH8hAWRDTkA)

---
###### Memory Card
![[Samsung_SaM_Notes_10_240515_182746_1.jpg]]

---
# Index
- [[#Definition of the Gauge Factor]]
- [[#~Real World Example • Standard Values for Metallic Strain Gauges]]
- [[#How is a Strian Gauge Made]]
- [[#How Transverse Sensitivity Affects a Strain Gauge]]
- [[#Temperature Effects]]
- [[#~Ex. Temperature Effects • Uniaxial Stress Case]]
- [[#Relative Variation of Resistance for Metals and Semiconductors]]

---
##### Definition of the Gauge Factor
![[Pasted image 20231127191427.png]]
- As we have seen the [[SaM - Piezoresistivity Effect|piezoresistivity effect for metal]] is: ${d\rho \over \rho} = c {dV \over V}$

So if we calculate the percentage variation of resisitivity of a metal strain gauge we obtain:
![[Pasted image 20231127191931.png]]
![[Pasted image 20231127191855.png]]

---
##### ~Real World Example • Standard Values for Metallic Strain Gauges
Also for strain gauges we always have that $\varepsilon_x$ is:
![[Pasted image 20231127192314.png]]
- $\mu \varepsilon$ is "microstrain" and is a conventional measurement unit that is equal to $10^{-6}$, since the strain is a pure number.
- The formula of strain gauge is really similar to [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen Equation for RTDs]].
- It is important to note however that for strain gauge $G\varepsilon_x$ is at most in the order of $0.1$, (or $10\%$ variation) so the variation of resistance is really small.<br>Instead for the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 sensor]] (a particular [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensor]]) the variation of resistance can even be $\times4$ (or $300\%$ variation) of its initial value. #IMPORTANTE 
- $R_0$ for the strain gauge can assume the values reported above, so between $[50\ohm \div 700\ohm]$.
- It is important to choose a material that has low TCR (Temperature Coefficient of Resistance), while we have seen for **RTDs** that the opposite is true.<br>The metals and alloy we choose for strain gauge have a TCR between $[10^{-5}°\text{C}^{-1} \div 10^{-6}°\text{C}^{-1}]$.


---
###### How is a Strian Gauge Made
The metal used to make a strain gauge is placed in a particular pattern:<br>![[Pasted image 20231128114715.png]]

In this way we can increase the "**parallel resistance**" $R_{\parallel}$, while keeping the "**perpendicular resistance**" $R_{\perp}$ to a low value.
![[Pasted image 20231128114747.png]]
- $R_{\parallel}$ is defined as the sum of all the **thin and long** parts of the total resistance.
- $R_{\perp}$ is defined as the sum of all the **thick and short** parts of the total resistance.
- $R_{\perp} \ll R_{\parallel}$ so $R_{\perp}$ can be ignored.

==This kind of structure allows to have a **small transverse sensitivity**, which means we only sense displacement in the $x$ direction, and almost in the $y$ direction==. 
==The sensitivity on the $y$ axis is $\lt 1\%\div 2\%$ with respect ot the sensitivity on the $x$ axis==.
![[Pasted image 20231128115340 1.png]]

There are many different "strain-sensitive alloy", here's a list of them:
![[Pasted image 20231128115340.png]]
- $D$ : **ISOELASTIC** (Dynamic Measurements)

---
##### How Transverse Sensitivity Affects a Strain Gauge
In case of **Uniaxial Stress**:
![[Pasted image 20231128120030.png]]
- $S_T$ is a factor to describe the **transverse sensitivity**, and is a ration between the ***transverse gain*** ($G_T$) and the ***normal gain*** ($G$)
- So the guage factor in case of **uniaxial stress** along the $x$ direction, is resduce by a factor of $(1-s\nu)$, due to the **transverse sensitivity** of the gauge sensor (due to how the strain gauge is built).<br>It can also be wrote as:$$G_V= G-G_T\cdot\nu$$Where:
	- $G_v$ is the true value of the gauge factor.
	- $G_T$ is the transverse gauge factor.
	- $\nu$ is the [[SaM - Young and Poisson Modulus|Poisson Modulus]]

While in case of **General Stress**:
![[Pasted image 20231128120746.png]]
I write it better:$$R=R_0\left(1+G \kern2px \varepsilon_l \kern2px \left(1+s\frac{\varepsilon_T}{\varepsilon_l}\right)\right)$$Which is identical to say:$$R=R_0\left(1+G \kern2px \varepsilon_l + G_T \kern3px \varepsilon_T \right)$$

---
##### Temperature Effects
![[Pasted image 20231128121053.png]]

---
##### ~Ex.: Temperature Effects • Uniaxial Stress Case
![[Pasted image 20231128121156.png]]

---
##### Relative Variation of Resistance for Metals and Semiconductors
Resitance for metal strain gauges varies both with the piezoresistive effect, and the geometrical effect:
![[Pasted image 20230610190005.png]]
- This formula comes from the [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|basic formula of resistance]] $\left(R = \rho{l\over S}\right)$, and since to obtain a [[SaM - Piezoresistivity Effect|piezoresistive effect]] we need to exert a certain **strain**, se we change the lenght ($l$) and surface area ($S$) respectivly by an infinitesimally small factor of $dl$ and $dS$.<br>So we can calculate the infinitesimally small variation of resistance ($\frac{dR}{R}$) using the shown formula, basically by deriving it where:
- $\frac{dR}{R}$ : ***relative variation of resistance***, or "*fractional change in resistance*".<br>Where:
	- $dR$ is the change in resistance.
	- $R$ is the inital resitance value.
- $\frac{d\rho}{\rho}$ : relative variation of resistivity (this is provoked by the **piezoresistive effect**)<br>Which is: ${d\rho \over \rho} = c {dV \over V}$
- $\frac{dl}{l}$ and $-\frac{dS}{S}$: these are the relative variation of lenght and relative variation of surface area.

Instead for semiconductors only due to the piezoresistive effect:
![[Pasted image 20230610190204.png]]
- The [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|basic formula]]: $R = \rho{l\over S}$ is true also for semiconductors, but this change in resistance can be negletcted since it is significantly smaller than its piezoresisity effect. #NOT_SURE_ABOUT_THIS 
