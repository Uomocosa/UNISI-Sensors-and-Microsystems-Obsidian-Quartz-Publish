##### ***Remeber***:

> - Apllying a current to a passive sensor (or even applying a current/voltage in general) will result in heat-dispersion, so if the temperature of the sensor is a relavant factor for determening the measure of the target, [[SaM - Self-Heating|self-heating]] can be a problem.
> - To reduce this problem we have seen a method, that we will call "***Train of Pulses***", which consists in changing the source from a **DC Voltage** to a **repeating square wave function** or "**train of pulses**".<br>This special function has 2 distinct periods:<br>![[Pasted image 20231124113031.png|500]]
> - $T$ : ***full period*** or normal defined period.
> - $T_{ON}$ : period in which the source feeds current into the system.
> - $\delta$ called the "***duty cycle***" is the ratio between this two periods.
> - ==In this case we need to read the output only during the $T_{ON}$ periods, otherwise we'll measuring nothing==.<br>So we need to have an electrical system fast enough to adapt to this pulses, which is usually possible.

> - To evaluate how much this approach reduces the effect of self-heating we need to:
> 	1. Construct the [[SaM - Thermal Lumped Parameter System|thermal lumped parameter system]]:<br>![[Pasted image 20230601170224.png|333]]<br>**NOTE**: The [[SaM - Lumped Parameter Systems|heat flux]] $\dot Q_S$ (*the flow quantity of the thermal lumped parameter system*), since we consider only the electronic circuit (we are evaluationg only the self-heating effect) is exaclty the **power** of the electronic circuit.
> 	2. To find exaclty how much the self-heating value is we need to find using the **laplace tranformation** $T(s)$ and isolate the part containg $\dot Q_S$, the result will be:$$\text{self-heating} \triangleq \Delta T_S(s) = \dot{Q}_S \kern2px \frac{R_{XS}}{1+R_{XS}\kern3px C_S}$$(*This is not so imporant*)<br> ==While it's #IMPORTANTE to remeber that the **PT100** as any other sensor suffers form self heating, in actual number the measured value changes of about $\simeq 0.5 {\text{°C} \over \text{mW}}$==.
> 	3. Since the self-heating depends directly to $P(t)$, if we reduce the **power** or **medium power**, we will reduce the self-heating effect, so we can calculate:<br>![[Pasted image 20231124120722.png|333]]
> 	4. So the final result is that, if we use a **train of pulses** instead of a **DC input**, we can reduce the self-heating effect by a factor of $\delta$ (the ***duty cycle***):<br>![[Pasted image 20230601171128.png|333]]

> - Often you find this kind of diagram to relate in logaritmic form the voltage and current:<br>![[Pasted image 20230601171409.png|400]]
> - Each diagonal line represent a different resistance value, or a value for power following the formulas:$$\log V = \log R + \log I$$and:$$\log V = \log P - \log I$$
> - This diagonal lines are **ideal**, but due to self-heating the relationship between $I$ and $V$ is not linear, as show under.
> - If I draw lines which describes different constant powers, you will have this behavior here, due to self-heating:<br>![[Pasted image 20230601171600.png|500]]<br>![[Pasted image 20230601171543.png|500]]> - You see that resistance remains with the same value until something happens due to the fact that the power is too high (self-heating), and the resistence value tend to diminsh.
> - Usually these diagrams are drawn wiht a $T_x$ constant, usally taken at ambient temperature ($25°C$), the medium being air.

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_5.jpg]]
![[Samsung_SaM_Notes_21_240516_160358_4.jpg]]

---
# Index
- [[#Train of Pulses]]
- [[#Thermal Circuit]]
- [[#Low Pass Function]]
- [[#Fundamental Frequency on Train of Pulses]]
- [[#DC Errors on Train of Pulses]]
- [[#~ Real World Example • How Data Sheet Represent Self-Heating]]

---
##### Train of Pulses
![[Pasted image 20230601170055.png]]

- ==The idea of having variables power for the resistance can be useful also to reduce the effect of self-eating==.  
- In fact, you can use for instance a current source which generates a train of pulses.  
- ==So we can draw our current which I input to the resistance, with a defined "**full period**" $T$ from one pulse to the other, and another much shorter period $T_{ON}$ where the generator is on (the period of a pulse of current)==.
- ==So, the **duty cycle** $\delta$ is defined as the $T_{ON}$ divided by the full period $T$==.  
- And obviously you have to perform the reading during the period $T_{ON}$.  
- So you should have an AD converter, which converts only in periods where the power is on.  
- ==And this means that you need something which synchronizes the excitation and the reading of the resistance==.

 >***Definition of Duty Cycle***:
 >==The duty cycle is a term commonly used in electronics and signal processing to describe the ratio of the time a signal is ON (active) compared to the total period of the signal.<br>It is often expressed as a percentage==.

---
##### Thermal Circuit
![[Pasted image 20230601170224.png]]
- Here you have an equivalent thermal system (or circuit), where you have your sensor, with temperature $T_s$ , and the thermal capacitance $C_s$ of the sensor,

![[Pasted image 20230601170417.png]]
- ==We have that the power $P(t)$ which is the heat flux ($\dot Q_s$) that we give to our resistance is equal to $R I^2(t)$.<br>$R$ will vary with temperature but we consider it constant or almost constant.
- So the temperature of the sensor ase we have already seen it is $T_s(s)$ (in Laplace domain)
- ==The first component of the $T_s(s)$ equation is the **error we have for self heating**==.  
- ==We can go to the freqency domain and write the error as $\Delta T_s(\omega)$==.
- ==$\tau$ recall is due to the product of the **thermal resistance** and the **sensor's thermal capacitance**==.
- As an example we consider $\tau$ as a *PT-100 surface film resistance*, that is something which is approximately $0.5\frac{°C}{mW}$, which is typical value that you can find.

So we have that the self heating effect (for a simple body+sensor example) is defined as:$$\Delta T_S(\omega) = \frac{P(\omega)R_{XS}}{1+j\omega s}$$

---
##### Low Pass Function
![[Pasted image 20230601170541.png]]
- The **error** (self-heating effect $\Delta T_S$) divided by the **power** you give to your sensor, in the frequency domain, it's a **low pass function**.


---
##### Fundamental Frequency on Train of Pulses
We have defined the power as $P(t) = \dot Q_S = RI^2$ 
Where $I(t)$ is defined as a train of pulses:
![[Pasted image 20230601170644.png]]
- ==So you will have a fundamental frequency $f_0$==

%%A train of pulses with fundamental frequency $f_0$ in frequency domain is equal to:
![[Pasted image 20230915174033.png]]
%%
Let's represent our $f_0$, and obviously also the higher harmonics ($2f_0$, $3f_0$, ...) all above the cutoff frequency of the thermal filter:<br>![[Pasted image 20230601170744.png]]
- Then the only thing which you will have, as a steady state response, is the average value, (the delta at $\omega = 0$), which represents the DC component of the power.

The dotted line represents the DC component of the generator:
![[Pasted image 20230601170757.png]]

We can evaluate it:
![[Pasted image 20230601170907.png]]
- ==So you have reduced the average power, with respect to the DC, by a factor which is given by the duty cycle $\delta$==.

---
##### DC Errors on Train of Pulses
Let's compere now the self-heating error on two different exitation, one pulsed (train of pulses we have seen now) and the other given by a DC power source:
![[Pasted image 20230601171128.png]]
- Both error are considered as "DC errors", what changes is the exitacion
- So by having a pulsed exitacion, instead of a DC exitation we will have reduced the error, by a factor of $\delta$ the duty cycle.

I need to read the resistance at the points where the generator is on, ==where for a brief moment the currnet is costant, that's why we call it still a DC error==:
![[Pasted image 20230601171139.png]]
- We need to have an electrical system fast enough to adapt to this pulses, which is usually possible.

---
##### ~ Real World Example • How Data Sheet Represent Self-Heating
Often you find this kind of diagram to relate in logaritmic form the voltage and current:
![[Pasted image 20230601171409.png]]
- Each diagonal line represent a different resistance value, or a value for power following the formulas:$$\log V = \log R + \log I$$and:$$\log V = \log P - \log I$$
- This diagonal lines are **ideal**, but due to self-heating the relationship between $I$ and $V$ is not linear, as show under.

If I draw lines which describes different constant powers, you will have this behavior here, due to self-heating:
![[Pasted image 20230601171600.png]]
![[Pasted image 20230601171543.png]]
- You see that resistance remains with the same value until something happens due to the fact that the power is too high (self-heating), and the resistence value tend to diminsh.
- Usually these diagrams are drawn wiht a $T_x$ constant, usally taken at ambient temperature ($25°C$), the medium being air.

---
