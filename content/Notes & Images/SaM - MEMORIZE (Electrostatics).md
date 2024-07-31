##### List of things to memorize:
![[SaM - Electrostatics]]

---
[[SaM - Electric Permittivity • Electric Susceptibility • Electric Field]]:$$\begin{array}{l}\text{Isotropic}:& \vec D = \kern1px\varepsilon \kern1px \vec E     \\     \text{Anisotropic}:& \vec D = \overline{\overline{\varepsilon}} \vec E \end{array}$$$$\varepsilon = \varepsilon_0 \kern2px \varepsilon_r$$$$\varepsilon_0 = 8.85 \times 10^{-12} \, {\text{C}^2 \text{m}^2 \over \text{N}}$$$$\varepsilon_r = 1 + \mathcal{X}$$$$\vec D = \varepsilon_0 \vec E + \vec P$$$$\vec P = \varepsilon_0 \mathcal{X} \vec E$$
For **Air**, **Water** and **PZT** (*Lead Zirconate Titanate*):
- $\varepsilon_{r_{\text{AIR}}}\approx 1$ 
- $\varepsilon_{r_{\text{WATER}}}\approx 80$ (@ $20 ° \text{C}$) 
- $\varepsilon_{r_{\text{PZT}}} \in [500 \div 6000]$ 
- _Also remember that in general: $\varepsilon_r \in [1 \div 6000]$_.
![[Pasted image 20230713163249.png|500]]
- ***Terminology***:
- $\varepsilon$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric permittivity]] $(\varepsilon = \varepsilon_0 \varepsilon_r)$
	- $\varepsilon_0$ : electric permittivity of the void $\left(\varepsilon_0 = 8.85 \cdot 10^{-12} \ {\text{C}^2 \text{m}^2 \over \text{N}}\right)$
	- $\varepsilon_r$ : relative electric permittivity
- $D$ : electric displacement field $\left(D = \varepsilon E\right)$
- $E$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric field]] $\left(\left[E\right] = {\text{V} \over \text{m}}\right)$
- $P$ : polarization vector $\left(P = \varepsilon_0 \mathcal{X} E\right)$
- $\mathcal{X}$ : electric susceptibility $\left(\varepsilon_r = 1 + \mathcal{X}\right)$
- **Si** : *Silicon*.
- **PZT** : *Lead Zirconate Titanate*.

---
[[SaM - Special Materials for the Electric Permittivity • Paraelectric, Piezoelectric, Ferroelectric]]:
***Paraelectric Materials***:<br>![[Pasted image 20230713163257.png|500]]

***Pyroelectric Materials***:<br>![[Pasted image 20230713163432.png|500]]

***Ferroelectric Materials***:<br>![[Pasted image 20230713163307.png|500]]

***Pyroelectric Materials***, ***pyroelectric effect***:<br>![[Lecture 8_230912_154531_1.jpg|500]]

---
[[SaM - Complex Electric Permittivity]]:$$\hat\varepsilon = \varepsilon' - j\varepsilon''$$***Static description***:$$\varepsilon_{\kern-2px \small DC} = \lim_{\omega \to 0}\hat{\varepsilon}(\omega)$$
***Examples***:
- *~Ex.: Water: $\varepsilon' = 78.5$, $\varepsilon'' = 2.25$ ⇒ ${\varepsilon'' \over \varepsilon'} \gg 1$*.
	- *So it's a **good conductor**, but a **poor dielectric** ([[SaM - Ultrasonic Waves|waves]] do not propagate well)*.
- *~Ex.: Vacum: $\varepsilon' = 1$, $\varepsilon'' = 0$ ⇒ ${\varepsilon'' \over \varepsilon'} = 0$*.
	- _So it's a **perfect dielectric**, **waves** do not attenuate, but does not conduct electricity, at all_.

***Ratio table***:<br>![[Pasted image 20230713163518.png|500]]<br>![[Pasted image 20230713163528.png|500]]

- ***Terminology***:
	- $\varepsilon_{\kern-2px \small DC}$ : static electric permittivity $\left( \varepsilon_{\kern-2px \small DC} = \lim_{\omega \to 0}\hat{\varepsilon}(\omega) \right)$
	- $\hat \varepsilon$ : complex electric permittivity $\left( \hat \varepsilon = \varepsilon' - j\varepsilon'' \right)$
		- $\varepsilon'$ : real electric permittivity (*represents the material's ability to store energy as an electric field*)
		- $\varepsilon''$ : imaginary electric permittivity (*represents the material's ability to dissipate energy as heat when subjected to an alternating electric field*)

---
[[SaM - Dielectric Materials]] (*Skipped*)
