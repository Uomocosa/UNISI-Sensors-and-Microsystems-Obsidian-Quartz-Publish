# Index
- [[#CMRR Formula]]
- [[#Steps to Calculate the CMRR]]
- [[#Why We Need a Good Differential Amplifier?]]
- [[#Instrumentational Amplifier]]
- [[#Definition of the 'Stages']]
- [[#Calculation of the CMRR of the Stage II]]
- [[#Calculation of the CMRR of the Stage I]]
- [[#Calculation of the CMRR of Both Stages]]
- [[#Calculation of the CMRR (Stage II) based on Design Rules]]
- [[#Calculation of the CMRR (Stage II) based on Resistance Tollerances]]
- [[#Calculation of the Complete CMRR]]
- [[#CMRR due to Circuit Topology]]

---
##### CMRR Formula
$$\text{CMRR} = \frac{|A_d|}{|A_C|} = \frac{A_2-A_1}{2(A_1+A_2)}$$

Where you need to remember:
- $V_0 = V_C A_C + V_d A_d$
- $V_d = V_2-V_1$ &$\kern3px$ $V_C = \frac{V_2+V_1}{2}$
- $A_d = \frac{A_2-A_1}{2}$  $\kern3px$&$\kern3px$ $A_C = A_2+A_1$
- Where: 
	- $A$ is the **gain**.
	- $_d$ means "***differential***".
	- $_C$ means "***common mode***".

A more clear explenation:
![[Pasted image 20230626201332.png]]
![[Pasted image 20230626201348.png]]

---
##### Steps to Calculate the CMRR
Operational Amplifier:
![[Pasted image 20230626201332.png]]

Simple Differential Operationa Amplifier, with four resistances:
![[Pasted image 20230718184020 1.png]]

So the steps to calculate the CMRR are:
1. Find $A_1$: $$A_1 = \left.\frac{V_0}{V_1}\right|_{V_2 = 0}$$
1. Find $A_2$:$$A_2 = \left.\frac{V_0}{V_2}\right|_{V_1 = 0}$$
2. Calculate the CMRR:$$\text{CMRR} = \frac{|A_d|}{|A_C|} = \frac{A_2-A_1}{2(A_1+A_2)}$$
---
##### Why We Need a Good Differential Amplifier?

Basic Differential Operational Amplifier:
![[Pasted image 20230626201332.png]]

We consider a simple scheme of a differential amplifer, considering some non linearities as the **common mode resistance** ($R_C$) and **differential resistance** ($R_D$).
![[Pasted image 20230626201429 1.png]]
- $V_c$ is the voltage on $R_{C1}$ (the common mode resistance)
- $V_d$ is the voltage on $R_{d}$ (the differential resistance)

We attach a **resistive bridge** before it:
![[Pasted image 20230626201510 1.png]]

If we consider $R_1 = R_2 = R_3 = R_4$, so $K = 1$, we will have that the output of this simple bridge+amplifier is equal to:
$$V_0' = A_d V_d + A_c \left(V_{CC} + \frac{V_d}{2}\right)$$
If we talk about **strain gauges**, also my "informative part", $V_d$ is **really small**, so I'll have a very small variation of the signal $V_d$ (maybe about some ***millivolts*** or even ***microvolts***).
==This is the reason why I need a good differential amplifier==.
Also a good differential amplifier is an amplifier with high CMRR, ideally infinte.

---
##### Instrumentational Amplifier
We start with defining the Instrumentational Amplifier:
- Here is the Circuit:
![[Pasted image 20231004153316.png]]
- And the Formula:$$V_{out} = (V_2 - V_1)\cdot\left(1+\frac{2R_1}{{R_{\text{gain}}}}\right)\frac{R_3}{R_2}$$
---
##### Definition of the 'Stages'
![[Pasted image 20230626201530.png]]

So, **Stage I**:
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHdxiVwxuxCqzbpHadu2bIXACQEqSIAePPMvDYkvCABZwKgGqBAghZKwuWVohgt5bFp06w+wEEELAIZjwKFbgdeQxcCQmDXh4KHCwUJF3MC5ZNFlIHWwElTAg9OQo8MEolgAnRJ0UBCkfD1y4UVi+Ow8aqGq4hvKGkQ4GzriS+SbuHo9y9o8B8oGRQrHSoviqSomZlqTPFXnRVr91Pj9h8pSqSW8ExVkMB1tZYnPyB30DAHJjWQJ47BAtSHEid90QPSdHkoJEgUCgAuoVCgUj9HCAAEoAcyewOkSAh0hUt3hACNkZIQGDkggAmCbr84bigA)<br>![[Pasted image 20231106192634.png]]

And **Stage II**:
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHdxiVPuxCqwXKCwAeIACzjyKMN3GE8IGUnHhFANQD2LAIZK8itIvFwl+EIrBImSMPHhRHd+6PApsncmHEe0VVWAagIEEAOSusoa44OKRHgEagEEEYQBOPGkoBmkC8Oz6lkIZlpLCqYXRqiYCxdlwuZXlEqZGwhz1zT7czZAsqYKdKKplKANOORx9SiN8VMOq3aWZs3nLNd0A5stDmdhojt1iaMTghL6Yx4QSaiAASkGuzSgIF8PPCEfxN4DBBK7YgUoYEGw2GeGAqV2ugBCCH4oI7McjYKRufzghIsIA)<br>![[Pasted image 20231106193135.png]]

---
##### Calculation of the CMRR of the Stage II

So remembering the formulas:
- $V_0 = V_C A_C + V_d A_d$
- $V_d = V_2-V_1$ &$\kern3px$ $V_C = \frac{V_2+V_1}{2}$
- $A_d = \frac{A_2-A_1}{2}$  $\kern3px$&$\kern3px$ $A_C = A_2+A_1$

And the structure of the Stage II:
![[Pasted image 20231106193135.png]]

We first calculate $A_1$ for $V_1'$:
$$V_0|_{V_2'=0} = -\frac{R_2}{R_1}\frac{\beta A_d}{1 + \beta A_d}V_1'$$

Then $A_2$ for $V_2'$:
$$V_0|_{V_1'=0} = \frac{R_4}{R_3+R_4}\frac{1}{\beta}\frac{\beta A_d}{1 + \beta A_d}V_2'$$
So: 
$$A_1 = -\frac{R_2}{R_1}\frac{\beta A_d}{1 + \beta A_d}$$
$$A_2 = \frac{R_4}{R_3+R_4}\frac{1}{\beta}\frac{\beta A_d}{1 + \beta A_d}$$
Finally:
$$\text{CMRR}_{II} = \large \frac{1}{2} \frac{\frac{R_4}{R_3+R_4}\frac{1}{\beta}+\frac{R_2}{R_1}}{\frac{R_4}{R_3+R_4}\frac{1}{\beta}-\frac{R_2}{R_1}}$$
Remember:
$$\beta = \frac{R_1}{R_1+R_2}$$

---
##### Calculation of the CMRR of the Stage I

We don't actually calculate the CMRR in this part.
Look at this structure:
![[Pasted image 20231106192634.png]]
We can define $V_2'-V_1'$ and $V_2'+V_1'$ based on $V_1$ and $V_2$, so:
$$(V_2' - V_1') = \frac{(2R_B + R_G)}{R_G}(V_2 - V_1)$$
But we also have that:
$$V_2'+V_1' = V_2+V_1$$

> **NOTE**: #IMPORTANTE 
> $R_B \simeq 50k\ohm$

---
##### Calculation of the CMRR of Both Stages
So we know that:
- $\text{CMRR}_{II} =  \large \frac{1}{2} \huge \frac{\frac{R_4}{R_3+R_4}\frac{1}{\beta}+\frac{R_2}{R_1}}{\frac{R_4}{R_3+R_4}\frac{1}{\beta}-\frac{R_2}{R_1}}$<br>
- $(V_2'- V_1') = \large \frac{(2R_B + R_G)}{R_G} \normalsize (V_2 - V_1)$
- $(V_2'+V_1') = 1\cdot(V_2+V_1)$

So we can say:
$$\begin{matrix} 
& \text{CMRR}_{TOT} = \\[5px]
& = \frac{1}{\frac{(2R_B + R_G)}{R_G}}\cdot \text{CMRR}_{II} \\[5px]
& = \frac{R_G}{2R_B+R_G}\cdot \text{CMRR}_{II}\end{matrix}$$
---
##### Calculation of the CMRR (Stage II) based on Design Rules
We start with the CMRR$_{II}$, more specifically with $A_{1_{II}}$ and $A_{2_{II}}$: 
$$A_{1_{II}} = -\frac{R_2}{R_1}\frac{\beta A_d}{1 + \beta A_d}$$
$$A_{2_{II}} = \frac{R_4}{R_3+R_4}\frac{1}{\beta}\frac{\beta A_d}{1 + \beta A_d}$$
We use the two following design rules: 
1. $A_1 = -A_2$ $\kern10px$ (So that we obtain an **infinite CMRR**)
2. $\large \frac{R_4}{R_3} = \frac{R_2}{R_1}  = \normalsize K$ $\kern10px$ (For **maximum sensitivity** #NOT_SURE_ABOUT_THIS )

So using the (1.) design rule:
$$\frac{R_2}{R_1} = \frac{R_4}{R_3+R_4}\frac{1}{\beta}$$
Using the (2.) design rule:
$$K = \frac{K}{1+K}(K+1)$$
We can find a value for $K$ and solve this.


---
##### Calculation of the CMRR (Stage II) based on Resistance Tollerances
Instead we complicate the problem:
1. We consider **different resistance ratios**, since having two resistence exactly equals is extreamly difficult:
	- $\large \frac{R_2}{R_1}  = \normalsize K$
	- $\large \frac{R_4}{R_3}  = \normalsize K'$
2. We consider the worst case scenario, where $K$ assumes the lowest possible value and $K'$ the highest, so we'll write it as:$$K' - K = 2\Delta K_{\max}$$
3. We define the **resistance tollerance**: $$\large \varepsilon_{\small R} \normalsize = \frac{\Delta R_{\max}}{R} = \frac{\Delta K_{\max}}{K}$$Where $\Delta K_{\max}$ is the maximum variation of the resistance ratio $K'-K$.
4. For **semplicity** we don't consider **no contribution** from the operational amplifier common mode rejection ratio, so I'm accounting only for the fact that the resistances ($R_1 ,\ \ldots ,\ R_4$) are not precisely what I would like to have from the design, so tolerances of the resistances.<br>That's why we will call it "$\text{CMRR}_{R}$".

Now we calculate the CMRR$_{R}$ based on this two new rules:
$$\text{CMRR}_{R} = \frac{1+K}{4 \kern2px \large \varepsilon_{\small R}}$$
So if we consieder the previous design rule: $R_1 = R_2 = R_3 = R_4$ (so $K = 1$)
We obtain that the last stage of the CMRR due only to resistance tollerances is given by:
$$\text{CMRR}_{R} = \frac{1}{2 \kern2px \large \varepsilon_{\small R}}$$
> **NOTE**: #IMPORTANTE 
> Usually we find: $\large \varepsilon_{\small R} \normalsize  = \frac{10^{-4}}{2}$
> So the $\text{CMRR} \simeq 10^{4}$<br>
> If these resistances are realized in an **integrated circuit** (**IC**), so with the same process, at the same moment, very close one to the other, then the matching is a parameter that could have a very high accuracy.
> This is the reason why we can't build our own instrumentation amplifier we have to buy it, in an integrated form.

---
##### Calculation of the Complete CMRR
So we have that if we consider the non-idealities of the Operational Amplifier, that is, if we consider that the $\text{CMRR}_{\text{OPAMP}} \neq \infty$ but instead it is equal to $\text{CMRR}_{\text{OPAMP}} = \frac{A_c}{2 A_d}$, we can sum the CMRR of the resistance tollerances and of the OP Amp like so:
$$\frac{1}{\text{CMRR}_{\text{(R+OPAMP)}}} = \frac{1}{\text{CMRR}_{\text{R}}} + \frac{1}{\text{CMRR}_{\text{OPAMP}}}$$This will give us the complete CMRR 

---
##### CMRR due to Circuit Topology
Consider a **resistive bridge** attached to an **ideal OP Amp**:
![[Pasted image 20230718184057 1.png]]
- For simplicity we simplifiy $V_C = V_{CC} + \frac{V_{TH}}{2}$ ⇒ to $V_C \simeq V_{CC}$.
- $\Delta R$ is the resisitve variation due to the sensor.

If we consider this ciruit topology even if the Amplifier is ideal, the CMRR will not be equal to infinity.

The CMRR only due to circuit topology will be given by:
$$\text{CMRR}_{\text{topology}} = \frac{A_d}{A_c + A_{c_{\text{topology}}}}$$Where:
$$A_{c_{\text{topology}}} = A_d\frac{\Delta R}{R_C}$$
So the Complete CMRR (also considering the resistance tollerances) is given by:
$$\frac{1}{\text{CMRR}} = \frac{1}{\text{CMRR}_{\text{topology}}} + \frac{1}{\text{CMRR}_{\text{R}}}$$

---
