# Index
- [[#Fermi Energy]]
- [[#Electron and Hole Density of States Functions]]
- [[#Density of Carriers]]
- [[#Density of Carriers in Different Medium]]
- [[#The Fermi-Dirac Dependence on Temperature]]
- [[#The Fermi's Energy Dependence on Temperature]]
- [[#Energy Gap and Carriers Dependance on Temperature]]
- [[#Instrinsic Mass Action Law]]

---
##### Fermi Energy
We started by saying that at $0$ **Kelvin** all the electrons are here in the **Valence Band**, and no electrons are in the **Conduction Band**. 
*What happens when we go to a temperature which is different from $0$ Kelvin?* 
To understand this, we have to look at the **probability that an electron occupies a given energy state (or level)**.

*==The **Fermi-Dirac distribution** $f_e(E)$ gives the ***probability*** that given a certain energy state with an energy level value $E$, this value $E$ is occupied by the electron*==, and it is defined as follows:$$f_e(E) = \frac{1}{1+ e^{\large \frac{ E-E_f}{kT}}}$$Where:
- $E$ is the energy that the electron takes. 
- $k$ is the **Boltzmann constant** $= 1.380649 \cdot 10^{-23} \, {\text{J}\over\text{K}}$. 
- $T$ is the temperature in **Kelvin**. 
- Whereas $E_F$ is a special energy level, which is called **Fermi's energy**. 

---
##### Electron and Hole Density of States Functions
Then we have to remeber the **density of states functions**, these represent the **density of states in the conduction band** (at a certain energy level $E$):
$$N_C(E) = \gamma\left(\frac{m_e^{*}}{m_0}\right)^{\frac{3}{2}}\sqrt{E-E_C}$$$N_C(E)$ quantifies how many **electron energy states** are available in the conduction band of a material at a particular energy level $E$.
It tells you how many electrons can potentially occupy a specific energy level in a material.

The **density of states in the valance band** (at a certain energy level $E$):$$N_V(E) = \gamma\left(\frac{m_h^{*}}{m_0}\right)^{\frac{3}{2}}\sqrt{E_V-E}$$Where:
- $\gamma=\frac{\sqrt{2} M_c}{\hbar^3 \pi^2}m_0^{\frac{3}{2}}$: a really small value that represents the "*effective density of states*". 
	- $\hbar$ : planck constant $=\frac{h}{2\pi} \approx 1.0545718 \times 10^{-34} \, \text{J}\cdot\text{s}$
- $m_e^{*}$ : effective mass of the **electron** (dependent on the material)
- $m_h^{*}$ : effective mass of the **hole** (dependent on the material)
- $m_0$ : mass of the electron $=9.10938356 \cdot 10^{-31} \, \text{kg}$
- $E_C$ : Conduction band lowest energy, (rember the CB in defined by $E_C$).
- $E_V$ : Valance band highest energy, (rember the VB in defined by $E_V$).
- This functions can be represented as:<br>![[Pasted image 20231007184939.png]]

---
##### Density of Carriers
Now if we wish to know the exact density of **free electrons** and **free holes**, so of **carriers** (free electrons and free holes will aid to conduction), we can integrate the density of states of the Conduction Band with the fermi energy like so, the density of **electrons** in the **Conduction Band** is:$$n_i = \int_{E_C}^{\infty} N_C(E) \kern2px f_e(E)\kern5px  dE$$And, the density of **holes** in the **Valence Band** is:$$p_i = \int_{-\infty}^{E_V} N_V(E) \kern2px \left(1-f_e(E)\right)\kern5px  dE$$Where:
- $\left(1-f_e(E)\right)$: is the probability of finding a hole at a certain energy $E$.

> **NOTE**: 
> We don't care about the electrons in the valance band and of holes in the conduction band, since **they are not carriers**. 

> **NOTE**:
> We are talking about $n_i$ and $p_i$, the suffix $_i$ stands for **instrinsic**.
> They are the density of carriers present in an **intrinsic semiconductor**, we will use them only for Silicon, but this formulas are general for every intrisic semiconductor.

We will find that:$$n_i = N_C \kern2px e^{-\large \frac{E_F-E_C}{kT}}$$And:$$p_i = N_V \kern2px e^{-\large \frac{E_V-E_F}{kT}}$$Where, this time:
- $N_C$ and $N_V$ do not depend on $E$, we can think of them as constants depending on the material and temperature.<br>For Silicon at room temperautre ($300°\text{K}$), we have that:
	- $N_C \simeq 2.8 \cdot 10^{19} \ \text{cm}^{-3}$
	- $N_V \simeq 1.83 \cdot 10^{19} \ \text{cm}^{-3}$
	- Also we have that $n_i \simeq 0.881 \cdot 10^{10} \ \text{cm}^{-3}$ 

---
##### Density of Carriers in Different Medium
So for intrinsic Silicon at room temperautre $n_i$ assumes the value that represent (approximately) an **insulator**.

Instead we have that, more generarly:
- For **metals** (conductors) we have that: $n_i \sim 10^{22} \ \text{cm}^{-3}$
- For **insulators** we have that: $n_i \sim 10 \ \text{cm}^{-3}$

Silicon at room temperature is about in the middle, but closer to an insulator than a metal.

---
##### The Fermi-Dirac Dependence on Temperature
We can see that the **Fermi-Dirac Distribution** depends on temperature looking at its formula:
![[Lecture 5_230908_172200_2.jpg]]
- If we work at $0°\text{K}$ the formula assumes a steep curve, in fact at $0°\text{K}$ we have all electrons in the valance band (under the fermi energy).
- However at higher temperatures the curve gets more smooth.

---
##### The Fermi's Energy Dependence on Temperature
Not only the Fermi-Dirac probability ($f_e(E)$) depends on temperature, but also the **Fermi's Energy** ($E_F$).

If we have an intrinsic semiconductor, at $0°\ \text{K}$ the Fermi's Energy is defined like so:$$E_F = E_i = \frac{E_C-E_V}{2}$$Where:
- $E_i$ is called the **Intrinsic Fermi's Energy**.
- $E_C - E_V = E_{gap}$, for silicon the gap spans for a total of $\simeq 1.12 \ \text{eV}$.
- For Intrinsic Silicon $E_i \simeq 0.56\ \text{eV}$

While more in general the **Fermi's Energy** is given by:$$E_F = \frac{E_C-E_V}{2}+\frac{3}{4}\kern2px k\kern2px T\kern2px \ln\left(\frac{m_e^{*}}{m_0}\right)$$Although for intrinsic Silicon the ratio between $m_e^{*}$ and $m_0$ is usually very close to $1$, so $E_F$ will be almost equal to $E_g$, however $E_g$ too depends on temperature.

---
##### Energy Gap and Carriers Dependance on Temperature
We have that:$$n_i \propto T^{\frac{3}{2}}\cdot e^{-\large \frac{E_g}{2kT}}$$While we can see the energy gap dependence on temperature as:$$E_g(T) = E_g(0) + \frac{\alpha T^2}{T+\beta}$$
So, since $n_i$ depends on $E_g$ we can draw this graph:
![[Pasted image 20231007194212.png]]
- We have that both $n_i$ and $E_g$ depend on temperature, so if we change the temperature too much we will have a change of behaviours, from **insulator** to **metal** (conductor) behaviour.

---
##### Instrinsic Mass Action Law
In intrinsic Semiconductors we have that: $$n_i^2 = p_i^2$$So we can simplify and say:$$n_i = p_i = \sqrt{N_C N_V}\kern3px e^{- \huge \frac{E_g}{2kT}}$$Where:
- $E_g$ is the energy gap, defined as $E_C-E_V$, for intrinsic silicon $\simeq 1.12 \ \text{eV}$.

> **NOTE**:
> In **intrinsic semiconducotrs** it is always true that:$$n_i=p_i$$

---
##### Complete Notes %% fold %%
![[Lecture 5_230908_172200_6.jpg]]
![[Lecture 5_230908_172200_1.jpg]]
![[Lecture 5_230908_172200_2.jpg]]
![[Lecture 5_230908_172200_3.jpg]]
- The integral for $p_i$ is wrong:$$N_V = \int_{-\infty}^{E_V} N_V(E) [1 - f_e(E)] dE$$

![[Lecture 5_230908_172200_3.jpg]]
![[Lecture 5_230908_172200_4.jpg]]
![[Pasted image 20230710172739.png]]
![[Pasted image 20230710172931.png]]
![[Pasted image 20230710172904.png]]
![[Lecture 5_230908_172200_5.jpg]]
![[Pasted image 20230710172954.png]]![[Lecture 5_230908_172200_6.jpg]]
![[Pasted image 20230710173005.png]]