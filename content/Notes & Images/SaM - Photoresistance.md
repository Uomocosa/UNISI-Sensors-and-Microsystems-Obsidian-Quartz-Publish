##### ***Remeber***:

> A "*photoresisitve device*" operates using the **photoelectric effect**.
> The photoelectric effect is based on the use of a semiconductor, where we have a certain energy gap $(E_g)$ less then the energy of a **photon** $(E)$.
> When a photon hits the material, it is able to free one electron from the valence band $(E_V)$ and promote it into the conduction band $(E_C)$. 
> So we have the creation of a free electron in the C.B. and a hole in the V.B.<br>![[Pasted image 20230718195828 1.png|500]]
> - $\lambda$ : wavelength.
> - $\nu$ : frequency.

> So given a certain wavelength $(\lambda)$ we will obatin a response in the form of more free carriers, so more conduction, ==⇒ **less resistance**==:<br>![[Pasted image 20230718195828 2.png]]
> - $h$ : Planck's constant, usually denoted as $\hbar$, approximately equal to: $6.626 \times 10^{-34} \kern2px J\cdot s$ (Joule-seconds).
> - $c$ : speed of light $\simeq 3 \cdot 10^{8} \frac{m}{s}$.
> - So we find a certain $\lambda_{\text{MAX}}$ that defines the maximum wavelenght, above which we will have no response, no change in resistance, we can find it as:$$\lambda_{\text{MAX}} = {c \hbar \over E_g}$$In reality there is also a $\lambda_{\text{MIN}}$, but we will not consider it.

> #IMPORTANTE 
> The visible light has a wavelength:$$0.4 \mu\text{m} \lt \lambda\lt 0.7 \mu\text{m} $$And a corresponding energy: $$1.78 \ \text{eV} \lt E \lt 2.8 \ \text{eV} $$
> A common **photoresistor** can be made out of $CdS$ or $CdSe$ semiconductors:
> - If we use the cadmium sulfide $(CdS)$ semiconductor, which as an $E_g = 2.4 \ \text{eV}$ we will have a $\lambda_{\text{MAX}} = 0.5 \mu \text{m}$.
> - Or we can use the cadmium selenide $(CdSe)$ semiconductor, which as an $E_g = 1.8 \ \text{eV}$ we will have a $\lambda_{\text{MAX}} = 0.6 \mu \text{m}$

> While **IR cameras** (*Infra-Red*) use $PbS$ or $PbSe$:
> - $PbS$ : lead sulfide, $E_g = 0.4 \ \text{eV}$ ⇒ $\lambda_{\text{MAX}} = 3 \mu \text{m}$.
> - $PbSe$ : lead selenide, $E_g = 1.5 \ \text{eV}$ ⇒ $\lambda_{\text{MAX}} = 0.83 \mu \text{m}$.

> The conductance of a **semiconductor** is calculated as:$$G = (q \kern1px n \mu_n + q \kern1px p \mu_p) \cdot \frac{A}{l}$$Where:
> - $G = {1 \over R}$ represents the conductance.
> - $q = -1.602 \times 10^{-19} \ \text{C}$ charge of the electron.

> #IMPORTANTE 
> For a photoresistance we will find that the resistance value is calculated using the relationship between the light and the resistance, proportional to the illuminance (measured in ***lux***, a flux of light):$$R = A_x E_{\nu}^{-\alpha}$$Where:
> - $E_{\nu}$ : **illuminance** is measured in ***lux*** (measure unit) $\left[\text{lux} = {\text{cd}\cdot \text{sr}\over\text{m}^2}\right]$
> 	- ***cd*** : candela (measure unit).
> 	- ***sr*** : steradian (measure unit).
> - ***$\alpha$*** : exponent, which is in the range $[0.9 ,\ 0.7]$.
> - ==A photoresistance is **non-linear sensors**, in fact is used more as a **light detector**==.

> So the resistance of a photoresistive material varies, a lot, the ration between the same material, once illuminated, once in darkness is:$${R_{\text{ILLUMINATED}} \over R_{\text{DARK}}} = 10^{-4}$$

> Finally, ==these are **slow devices**, and they show **hysteresis**==.
> Their [[SaM - Rise Time|rise time]] $\tau$ is:$$\tau_{63\%} \approx 10 \ \text{ms}$$Meaning that usually it takes about 10 milliseconds, to have a $63\%$ variation with respecto to the final value.
> *They are used for threshold measurement, for photography and sometimes also for infrared cameras*.

---
###### Memory Card
![[Samsung_SaM_Notes_10_240515_182746_1.jpg]]

---
![[Pasted image 20230718195812.png]]
This device operates using the **photoelectric effect**.
The photoelectric effect is based on the use of a semiconductor, where we have a certain energy gap:
![[Pasted image 20230718195828.png]]
- $h$ : Planck's constant, usually denoted as $\hbar$, approximately equal to $6.626 \times 10^{-34} \kern2px J\cdot s$ (Joule-seconds)
- $c$ : speed of ligth $\simeq 3 \cdot 10^{8} \frac{m}{s}$
- $\lambda$ : wavelength
- $\nu$ : frequency

If this energy is larger than the energy gap, the photon hitting the material is able to free one electron from the valence band ($E_V$) and promote it into the conduction band ($E_C$). 
So we have the creation of a free electron in the C.B. and a hole in the V.B.

%%Given a certain energy gap $E_g$ we have the **maximum wavelength** ($\lambda_{MAX}$) which is possible to use in order to get a response. %%


---
##### ~Ex.: Photoresistance for Visible Light
![[Pasted image 20230718195841.png]]
![[Pasted image 20230718195853.png]]
- **IR**: *Infra-Red* 
- $$G = (a n \mu_n + a p \mu_p) \cdot \frac{A}{l}$$
	- $G$ represents the conductance.
	- $q$ charge of the electron.
	- $n$ represents the electron concentration.
	- $\mu_n$ represents the electron mobility.
	- $p$ represents the hole concentration.
	- $\mu_p$ represents the hole mobility.
	- $A$ represents the cross-sectional area.
	- $l$ represents the length.

![[Pasted image 20230718195904.png]]
- But the phenomena of **recombination** is really slow.
- $R$: resistance.
- The relationship between the light and the resistance, proportional to the illuminance (measured in ***lux***, a flux of light)
- $$R = \frac{1}{G} = A_x E_{\nu}^{-\alpha}$$
	- $E_{\nu}$ is measured in ***lux*** (measure unit).
	- ***cd*** : candela (measure unit)
	- ***sr*** : steradian (measure unit)
	- ***$\alpha$*** : exponent, which is in the range $[0.9 ,\ 0.7]$.

So the resistance of a photoresistive material varies, and a lot, this is the ration between the same material, once illuminated, once in darkness:
![[Pasted image 20230718195918.png]]
- $R_{ILL}$: resistance of a photoelectric material when illuminated
- $R_{DARK}$: resistance of the same photoelectric material when in darkness (not illuminated)
- And then the last thing we have to see to see is that ==these are **slow devices**, and they show **hysteresis**==.<br>Usually, you find the value of the $\tau$ constant, which gives you a $63\%$ variation with respect to the final condition, which is about 10 milliseconds.
- *They are used for threshold measurement, for photography and sometimes also for infrared cameras*.