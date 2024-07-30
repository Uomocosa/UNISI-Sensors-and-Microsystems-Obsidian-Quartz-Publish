##### List of things to memorize:
![[SaM - Capacitive Sensors]]

---
###### [[SaM - Types of Capacitive Sensors]]
- ***Capacitive sensor***:
	- [[SaM - Capacitive Displacement Sensors|displacement]] or [[SaM - Capacitive Proximity Sensors|proximity]] sensors.
	- [[SaM - Capacitive Level Sensor|level sensors]].
	- [[SaM - Capacitive (Ferroelectric) Temperature Sensor|temperature sensors]].
- ***Capacitive primary sensors***:
	- [[SaM - MEMS Membranes|Membranes (MEMS)]]
	- [[SaM - Deformable Structures|Deformable strucutre (MEMS)]].
	- [[SaM - MEMS Cantilever|Cantilever (MEMS)]].
	- [[SaM - Capacitive Accelerometer|Capacitive accelerometer]].
	- [[SaM - MEMS Capacitive Pressure Sensor|Preassure sensors]].
- ***Advantages ofcapacitive sensors***:
	- _They are **non-contact**_.
	- _**Good [[SaM - Resolution|resolution]] for small ranges**, in the order $\sim [10^{-5}\div 10^{-6}]$_.
	- _**Very simple structure**, the sensor is just a metallic plate, it doesn't matter which kind of metal, usually, and it doesn't matter the shape, two metallic plate are enough to build a capacitance_.
- ***Disadvantages of capacitive sensors***:
	- _**Small capacitance value**_.
	- _They can work only for small ranges (small distances), this is one of the reasons because they are called proximity sensors_.<br>_We can write this simple relationship in order understand_:<br>==_The ratio: range (maximum distance that can be measured), diameter of the probe (thinking about a circular probe, a circular plate), is roughly_==:$${\text{range} \over \text{probe's diameter}} = {1 \over 8}$$
	- _Capacitive proximity sensors are sensitive to: **dirt**, **humidity**, and to **extreme temperature** and **extreme preassure** (found in industrial applications)_.
- ***Parassitic resistance at low frequency and parasisitic capacitances at high frequencies***:<br>![[Pasted image 20230718200900 1.png|333]]
- ***Example with parasisitic resisitances $(R_1 ,\ R_2)$***:<br>![[Pasted image 20230718200900 2.png|333]]
- ***Output $(V_o)$ at regime***:$$V_{\infty} = {R_{2} \over R_{1} + R_{2}} \kern2px V_{DC}$$(_Depends ONLY on the parasistic reisistances, **really bad**_).
- ***Output $(V_o)$ at the start***:$$V_{0} = {C \over C + C_R} \kern2px V_{DC}$$(_Depends ONLY on the sensor and reference capacitance, **good**_).
- ***Real World Measures***:
	- Capacitice sensor measure a value of: $C = 1 \ \text{pF}$. $\left( \text{Remember} \ : \ 1 \ \text{p} = 10^{-12} \right)$<br>We measure with a frequency of $100 \ \text{kHz}$.<br>⇒ The resulting impedance $|Z| = {1 \over \omega C}$ is equal to $10 \ \text{M}\ohm$, which is **realy large**.<br>⇒ This high impedance will be a problem: _**if the [[SaM - Front-End Electronics • Read-Out Electronics|front end electronic]] it's not well designed, it will load the source**_.<br>Moreover, with high impedance sources, you will have **[[SaM - Electrical Noise|electrical noise]]**.
	- Capacitive sensor are small $\sim 1 \ \text{cm}^2$.
	- They are used really close to the target (talking about [[SaM - Capacitive Proximity Sensors|proximity sensors]]) $\sim 1 \ \text{mm}$.

---
###### [[SaM - Capacitive Displacement Sensors]]
- ***Simplest capacitive displacement sensors***:<br>![[Pasted image 20230718200533.png]]<br>![[Pasted image 20230718200542.png]]<br>![[Pasted image 20230718200551.png]]

---
###### [[SaM - Capacitive Proximity Sensors]]
- ***Structure***:<br>![[Pasted image 20230718200559.png|500]]
- ***Basic formula***:$$C = \varepsilon \frac{A}{d}$$
- ***Graph***:<br>![[Pasted image 20230718200617.png|333]]
- ***With a large, conductive target, which is also not grounded***:<br>![[Pasted image 20230718200647.png|500]]
- ***Measured capacitance formula***:$$C_{\text{MEAS}} = {C_S C_{GT} \over C_S + C_{GT}} \approx C_S$$If the **sensor is small** (if its area $A$ is small) relative to the **large target** ⇒ $C_S \ll C_{GT}$ and $C_{MEAS} \simeq C_S$.<br>⇒ ==_So it's like having a grounded conductive target (**good**)_==.
- ***Proximity sensor with non-conductive target***:<br>(_Can be done if the [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric permittivity]] of the target is different from the one of the vacuum_)<br>![[Pasted image 20230718200707 - Copia.png|500]]
- ***Real World Measures***:
	- A **circular** capacitive proximity sensor with radius $r = 10 \text{ mm}$, measuring an object $1 \text{ mm}$ away will assume a capacitance of about $2.7 \text{ pF}$.
	- ***Impedance of a capacitive sensor***:$$| Z | = {1 \over \omega C_0}$$==**Small capacitance** means **high impedance**==.
		- This can be mitigated by operating this sensor at **high frequency**.<br>**HOWEVER**: we know that the higher the frequency the most critical is the design of the electronics
		- We have to cope between these two requirements: **keep this impedance small enough to be measured** and to operate at a **not too high frequencies**.

---
###### [[SaM - MEMS Capacitive Pressure Sensor]]
- ***Structure***:<br>![[Pasted image 20230718200720 1.png]]
- _Both the membrane and the fixed plate are **conductive** and act as the plates of the sensor_.
- ***Formula***:$$C_0(1 + x)$$Where: $x$ is a linear function of the differential preassure:$$x = \alpha \kern2px (P_1-P_2)$$

---
###### [[SaM - Capacitive Accelerometer]]
- ***Structure***:<br>![[Pasted image 20230718200738 1.png]]
- ***Formula***:$$C = {C_0 \over 1 + \alpha \cdot a_0}$$
- ***Terminology***:
	- $C_0$ : capacitance value at rest.
	- $a_0$ : constant accerelation.
	- $\alpha$ : constant [[SaM - Sensitivity|sensitivity]] $\left(\alpha = {M_S \over k \cdot d_0}\right)$
		- $M_S$ : sismic mass.
		- $k$ : elastic constant.
		- $d_0$ : distance between the plate, at rest.

---
###### [[SaM - Capacitive Level Sensor]]
- ***Structure***:<br>![[Pasted image 20230718200747 1.png|500]]
- ***Formula for non-ionic liquid***:$$\begin{array}{l} C &=& C_1 + C_2 \\ &=& {\huge{2\pi \varepsilon_1 h \over \ln{\left(b\over a\right)}}} + {\huge{2\pi \varepsilon_0 (l-h) \over \ln{\left(b\over a\right)}}}      \end{array}$$
- ***Formual for ionic liquids***:$$C = {\varepsilon_0 A \over d}$$Where:<br>![[Pasted image 20230718200754.png|333]]
- _Non-ionic liquids act like an insulator, like hetanol and water_.
---
###### [[SaM - Capacitive Humidity Sensor]]
- ***Structure***:<br>![[Pasted image 20240214110835.png|500]]
- ***Formula***:$$C = {A \over d}\varepsilon(\text{RH})$$
- ***Real World Measures***:
	- Variation of capacitance due to the humidity percentage:$${\Delta C \over C} = 1.7 \ {\text{pF} \over \text{RH\%}}$$
	- Typical capacitance value:$$375 \ \text{pF} + 1.7 \ {\text{pF} \over \text{RH\%}}\cdot  \text{RH\%}$$(_This is a measurable capacitance, it is big enough, **good**)

---
###### [[SaM - Capacitive (Ferroelectric) Temperature Sensor]]
- ***Structure***:<br>![[Pasted image 20230718200818 - Copy 1.png]]
- ***[[SaM - Special Materials for the Electric Permittivity • Paraelectric, Piezoelectric, Ferroelectric|Ferroelectric material]]'s [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric permittivity]]***:$$\varepsilon = {K \over T - T_C}$$
- ***Real World Masures***:
	- These temperature primary sensors are **really rare**, since there are many other [[SaM - Different Types of Temperature Sensors|types of sensors]], among which **[[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensors]] are very effective**.
- ***Terminology***:
	- $K$ : constant depending on the material, we have not seen it in details.
	- $T$ : temperature (as always in $\left[°K\right]$)
	- $T_c$  : [[SaM - Compact Piezoelectric Coefficient Matrix for PZT • Dependence of Piezoelectricity on Temperature • Curie Temperature|Curie temperature]].

---
###### [[SaM - Readout Electronics for Capacitive Sensors (FM & AM Oscillators)]]
- We need to distinguish between:
	1. **Low frequency signals** or DC signals.<br>***Read-out for low frequency signals***:
		1. [[SaM - FM (Frequency Modulation) Based on Oscillators|FM: Frequency Modulation]] which uses a **grounded sensor**.
		2. [[SaM - Complete AM (Amplitude Modulation) Circuit|AM: Amplitude Modulation]] which uses an **unreferenced sensor**.
	2. **High frequency signals**.<br>***Read-out for high frequency signals***:
		1. [[SaM - High Frequency (AC) Signals|DC exitation]].
- For **low frequency signals**, we will need an **AC exitation**.<br>The frequency of the excitation ($f_{exc}$) has to be much larger than the maximum signal frequency ($f_{S_{MAX}}$), it should not be a problem since it's a low frequecny signal.<br>Since the signal $g(t)$ varies slowly, the capacitance takes a value which is constant for a long time.<br>This time is enough to allow the **loss of the charge** which is stored in the capacitors due to the parasitic resistances.



---
###### [[SaM - Square Wave Oscillator]]
- ***Structure***:<br>![[Pasted image 20230921232009.png|333]]
- ***Formula***:$$T = 2RC \cdot \ln\left({1-\beta \over 1+\beta}\right)$$
---
###### [[SaM - FM (Frequency Modulation) Based on Oscillators]]
- ***Using a [[SaM - Square Wave Oscillator|square wave oscillator]]***:<br>![[Pasted image 20230719105145 1.png|500]]
- ***Formula***:$$T = 2RC \cdot \ln\left(\frac{1+\beta}{1-\beta}\right)$$
- ***Frequency of an FM modulated signal***:$$f(t) = f_0\left(1+\frac{f_A}{f_0}x(t)\right)$$
- ***FM modulation using an [[SaM - Integrator Circuit|integrator]]***:<br>(_For instance if I have $x(t)$ which is a slowly growing invariant signal, then the frequency would increase a litte over time._)<br>![[Pasted image 20230719105202.png|500]]
- ***Bandwidth of the FM modulated signal***:<br>![[Pasted image 20230719105215.png|500]]<br>Where:
	- $\Delta f_{MAX} = f_A \cdot x_{MAX}$.
	- And $f_A$ comes from: $f(t) = f_0+f_A \kern2px x(t)$.
- _Since FM transforms a the physical input variation into a variation of frequency, **it is a very robust solution to reject noise**_.
- ***Complete FM Circuit***:<br>![[Pasted image 20230719105215 - Copia 1.png]]
	- _The sensor is part of the oscillator_.
	- _The **FM Demodulator** gives as output a voltage related to the frequency in input_.
- ***Real World Measures***:
	- FM is used for signals which can be static but also they have a large bandwidth up to $100 \ \text{kHz}$
	- The typical value for $f_0$ is $2 \ \text{MHz}$ (much larger than the maximum signal frequency).

---
###### [[SaM - AM (Amplitude Modulation) Based on Oscillators]]
- ***Simplest circuit for AM (Amplitude Modulation)***:<br>![[Pasted image 20230719105223 1.png|500]]
- ***Output***:$$V_o(t) = \frac{C_0}{C_R}(1+x) \cdot V_g$$Where: $V_g = V \sin(2\pi f_0 \kern2px t + \varphi)$
- ***General formula of the AM modulation***:$$V_0(t) = V_R\kern2px[1+mx(t)] \sin(2\pi f_0 \kern2px t + \varphi)$$Where: $V_R = V\cdot {C_0 \over C_R}$
- ***Spectrum analysis***:<br>![[Pasted image 20230719105232 1.png|500]]
- ***Good circuits for AM modulation***:
	- [[SaM - Current Amplifier|Current]] or [[SaM - Charge Amplifier|charge amplifiers]].
	- AC [[SaM - Resistive Bridge • Wheatstone|bridges]].
	- Voltage dividers.

---
###### [[SaM - AM Modulation with 2 Sensors • Carrier Amplifier]]
- ***Circuit***:<br>![[Pasted image 20230719105256 1.png|500]]
- ***Sensors***:$$C_1 = {{C_0 \over 1 + x}}, \kern20px  C_2 = {{C_0 \over 1 - x}}$$
- ***Output***:$$V_{out} = V_g \left({Z_f \over Z_1} - {Z_f \over Z_2}\right)$$
- ***Final formula***:$$V_{out} = V{\kern-4px {\small{g}}} \kern2px {R_f \over 1 + j \omega R_f C_f} (j \omega2 C_0 \kern2px x)$$
- ***For $f_0 \gg f_{S_{MAX}}$***:$$V_{out} \approx - \frac{2 \kern2px C_0 \kern2px}{C_f}\kern2px |x|$$(_If I select a value for $C_f$ too large with respect to $C_0$ than I'll have a very small signal, **not good**_).<br>(_Since this is an [[SaM - Readout Electronics for Capacitive Sensors (FM & AM Oscillators)|FM modulation]], we will lose sign of $x$_).
- ***Bode graph***:<br>![[Pasted image 20230719105325.png|500]]
- ***Complete circuit with sign-recovery***:<br>![[Pasted image 20230719105428.png|500]]
- ***Real World Measures***:
	- $x \in [0,\ 1]$, also $x \ll 1$

---
###### [[SaM - Complete AM (Amplitude Modulation) Circuit]]
- ***Circuit***:<br>![[Pasted image 20230719105428.png|500]]
- _This is a differential circuit, since_:
	- $C_1 = \frac{C_0}{1+x}$
	- $C_2 = \frac{C_0}{1-x}$
- ***Pre-filtered formula***:$$V_0 = -{2C_0\over C_f}|x|$$
- ***Bode graph***:<br>![[Pasted image 20230719105436.png|500]]
	- ${1 \over 2\pi R_f C_f}$ is the lower frequency limit, defined by the [[SaM - Charge Amplifier|feedback impedance]], our frequency $f$ must be higher than this.

---

![[SaM - MEMORIZE (Amplifiers)#SaM - Carrier Amplifier]]
######
###### [[SaM - Low Pass Filter]]
- ***Circuit***:<br>![[Pasted image 20231130191754.png|333]]
- ***[Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEBmATNA7AhAOBjVIAWfbEfc8ycgUwFowwAoAJ3AE5UOvUcduoVOEwDGIXvzCdxfFMgBsgmPDjs16jZvYgi0dmGQIMkDPJzFUqZBEhMA7jMnSFTrrYcS5il16j3HvlJcyAp+AG4CIYpBAtQQRNRISNQwCEwADihmkdlRKEpMCcg6aOIJ5PLUyMSC8gD68kR1kHUJ7Dh1YC0wYHUMnYWQxdSo5WC8KDWJDU0tbR1dzbBD4wh9vah1a8hMAPYgio2C8+Ap0Db5yZQ7QA)***:<br>![[Pasted image 20240128162613.png]]
---
###### [[SaM - Switched Capacitors]]
- ***Circuit***:<br>(_It can be used to **increase the capacitance value**, with respect to the sensor's capacitance, without changing the actual capacitance_)<br>![[Pasted image 20230719105612 1.png|500]]
- ***Workings***:
	1. ***START*** : $S_3$ : **closed**, so that we start from $0 \kern2px V$.
	2. ***$C_S$ CHARGES***: ($S_1$: **ON**, $S_2$: **OFF**, $S_3$: **OFF**).
	3. ***$C_S$ SHARE ITS CHARGE WITH $C_E$*** : ($S_1$: ***OFF***, $S_2$: ***ON***, $S_3$: ***OFF***).
	4. _repeat (2.) and (3.), $n$ times_.
- ***Output at each step, relative to previous step***:$$V_{out}^{(n)} = \frac{C_S V_R + C_R V_{out}^{(n-1)}}{C_S + C_R}$$
- ***Absolute output formula***:$$V_{out}^{(n)} = n \cdot C_S \cdot \Delta Q_n$$Where: $$\Delta Q_n = \frac{V_R}{C_R}$$
- ***Graph***:<br>(*If I limit the measurement ratio to $n_{MAX}$, opprotunaly choosen, I will remain in the linear range*)<br>![[Pasted image 20230719105635.png]]

---
###### 
![[SaM - MEMORIZE (Front-End Electronics • Read-Out Electronics)#SaM - Sigma-Delta Converter (AD Converter)]]
###### 
###### [[SaM - High Frequency (AC) Signals]]
- ***Pure AC input signal***:<br>![[Pasted image 20230719105735 1.png|333]]
- ***DC exitation circuit***:<br>![[Pasted image 20231119190855.png]]
- ***Sensors***:$$C_1 = {{C_0 \over 1 + x}}, \kern20px  C_2 = {{C_0 \over 1 - x}}$$
- ***Output***:$$V_{out} = {V_{DC}\over 2}(1-x)$$
- _~Ex.: capacitive microphone electrical model_:<br>![[Pasted image 20230719105807 1.png|333]]
- ***Needed force to move the microphone's plate***:$$F \propto \frac{A}{h^2}$$The needed DC exitation to get a readable signal would be really high, $V_{DC}$ usually, it's a large value ($\sim 100 \kern2px V$).

---
###### [[SaM ~ Examples of Capacitive Sensors]]
(_Skipped_)
