# Index
- [[#Calculation of the Electro-Neutrality]]
- [[#~Ex. n-type Doped Silicon]]

---
##### Calculation of the Electro-Neutrality
Like we have done for **intrisic Silicon**, when we calculated the [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature#Density of Carriers|Density of Carriers]], we will use the same formula, however in this case we have a different formula for the [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature#Electron and Hole Density of States Functions|Electron and Hole Density of States Functions]], since we are talking about **extrinsic** or **doped** Silicon.

So starting with the new "***Electron and Hole Density of States Functions***":$$N_C'(E) = N_C(E) + N_A \cdot  \delta(E-E_A)$$And:$$N_V'(E) = N_V(E) + N_D \cdot  \delta(E-E_D)$$Where:
- $N_A \cdot  \delta(E-E_A)$ and $N_D \cdot  \delta(E-E_D)$ represents the single **extrinsic energy level** added by doping the material.<br>$\delta(E)$ in this case is the **Dirac's Delta**.

So given this changed Density of States, we continue with the calculation of the density carriers, the density of **electrons** in the **Conduction Band** will be:$$n = \int_{E_C}^{\infty} N_C'(E) \kern2px f_e(E)\kern5px  dE$$And, the density of **holes** in the **Valence Band** will be:$$p = \int_{-\infty}^{E_V} N_V'(E) \kern2px \left(1-f_e(E)\right)\kern5px  dE$$Where:
- $\left(1-f_e(E)\right)$: is the probability of finding a hole at a certain energy $E$.

---
##### ~Ex.: n-type Doped Silicon
Let's take a look at the **n-type** doped Silicon, so: $N_A \ \text{or} \ N_A^- = 0$, and:$$n = p + N_D^+$$
The only thing to remember is that when calculating the integral for the dopant, we need to use the "**Degeneracy Fermi-Dirac Function**" ($f_D(E$):
$$N_D^+ = \int_{\infty}^{\infty} N_D \cdot \delta(E-E_D) (1-f_D(E)) \kern5px dE$$Where:$$f_D = \frac{1}{1+\frac{\large1}{\large g_D}\cdot e^{\large\frac{E-E_F}{kT}}}$$And:$$1-f_D = \frac{1}{1+g_D\cdot e^{\large\frac{E-E_F}{kT}}}$$Where:
- $g_D$ is the "***degeneracy factor***".

So, at the end we will obtain:$$n = N_C \cdot e^{-\large\frac{E_C-E_F}{kT}}$$(Same formula as in the [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature#Density of Carriers|intrisic case]])

But also:$$n = N_V \cdot e^{-\large\frac{E_F-E_V}{kT}} + N_D^+$$We can also calculate:$$N_D^+ = \frac{N_D}{1+g_D\cdot e^{\large\frac{E-E_F}{kT}}}$$Where:
- Like in the intrinsic case, $N_C$ and $N_V$ do not depend on $E$, we can think of them as constants depending on the material and temperature.

==I can see $n$ as the **number of electron which you have in the conduction band**==. 
==But also I see $n$ as the sum of the hole that left behind this electron here, which says that this electron here comes either from the valence band or from the donors==. 

==By doping I transform material which is approximately an insulator at room temperature, into a conductor (even a good conductor)==.

Remeber that the [[SaM - Mass Action Law|Mass Action Law]] needs to be respected, so by doping we have "transformed" some holes in electrons or vice-versa.

---
##### Complete Notes %% fold %%
![[Lecture 5_230908_172200_7.jpg]]
![[Lecture 5_230908_172200_8.jpg]]![[Pasted image 20230710173123.png]]
![[Pasted image 20230710173133.png]]
![[Pasted image 20230710173207.png]]
![[Pasted image 20230710173218.png]]
