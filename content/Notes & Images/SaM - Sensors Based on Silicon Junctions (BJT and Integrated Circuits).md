##### ***Remeber***:

> This kind of devices are **absolute temperature sensors**, and we can find integrated circuits which behave **linearly**, and have **very good performances**.<br>However they have a **limited temperature range**, which is ==**the usual temperature range for integrated circuit which goes up to 150 degrees**== or something like this

> [[SaM - Fast Recap on BJT • Bipolar Junction Transistor|BjT]] used as a **Constant Current Generator**:<br>![[Pasted image 20230719123638 1.png|250]]
> - Specifically here we have an **npn transistor**, remeber that: **C** is the **collector**, **E** the **emitter**, and **B** the **base**.
> - ==There is a short-circuit between the base and the collector, therefore this device operates in the **active region**== (since $V_{BC} = 0 \ \text{V}$).
> - The formula for a BjT in active region is: #IMPORTANTE$$V_{out} = V_{BE} = \frac{kT}{q}\ln\left({I_C \over I_S}\right) $$
> - If we use some standard values, we find: #IMPORTANTE 
> 	- For $T = T_A$ (ambience temperature), so $300\ \text{°K}$.
> 	- $V_{BE} = V_{out} = 600 \ \text{mV}$.
> 	- The dependency on temperature is actually **non-linear**, due to the dependency of $I_S$ on temperature, this has to be comensated.
> 	- More specifically:
> 		- Ideally its [[SaM - Sensitivity|sensitivity]] would be $2 {\text{mV} \over \text{°K}}$.
> 		- Actually around $300°K$ if $I_S$ is not compensated, we have $\alpha = -4 {\text{mV} \over \text{°K}}$. #NOT_SURE_ABOUT_THIS (It is a huge difference)

---
###### Memory Card
![[Samsung_SaM_Notes_25_240516_113814_1 1.jpg]]

---
Now we will see that there are also another class of sensors which can be conveniently placed here but finds also many other applications.
And these are sensors based on **silicon junctions**. 

This kind of devices are **absolute temperature sensors** and there actually are integrated circuits which behave **linearly**, and have **very good performances**.
But have a **limited temperature range** to the **usual temperature range for integrated circuit which goes up to 150 degrees** or something like this.
We will know see a simple example, which unfortunatly will not behave linearly.

The basic idea is this one, first we consider a BJT:
![[Pasted image 20230719123638.png]]
- Remember this is the **collector** ($C$), the **emitter** ($E$) and the **base** ($B$).
- There is a short circuit between the base and the collector, therefore this device operates in the **active region**.

The formula which governs the BJT is:
![[Pasted image 20230719123649.png]]
- $K$ is the **Boltzmann constant**
- $q$ is the **charge of the electron**. 
- $I_S$ is the **reverse saturation current**.
- $I_C$ is the collector's current, and it's **related to the density of the intrinsic carriers, the minority carriers**.
- $N_A$ is the **density of the hole in the base**
- $D_n$ is the **diffusion coefficient**
- $A_q$ is the **emitter area**, and $w$ is the **width of the base**.

So, using the formula for the number of free electrons ($n_i$):
![[Pasted image 20230719123656.png]]
- $E_g$ : **energy gap**, can be considered approximated constant. 
- I don't know what we use the $n_i$ formula for.
- So at the end it will be that: $$V_{out} = \frac{KT}{q}\ln\left(\frac{I_C}{I_S}\right)$$
So for $T=T_A=300°K$ (ambience temperature) and using some standard values for the other variables, we have: 
![[Pasted image 20230719123723.png]]
- We have a stronger influence due to the variation of this current here which makes this behavior here **not linear**.<br>⇒ therefore it should be compensated.
- There are some integrated circuit which exploits the dependence of the conductance in a BJT due to temperature, tho they are a little bit more complex,  they encompass also a compensation strategy for the dependence of $I_S$ on temperature.

---