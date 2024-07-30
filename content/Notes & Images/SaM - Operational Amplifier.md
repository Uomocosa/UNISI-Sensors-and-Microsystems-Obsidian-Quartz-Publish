##### ***Remeber***:

> - ***Non-Idealities of Operational Amplifier***
> 	- $Z_{in}$ : **input resistance**, $Z_{in} \in [100 \ \text{k} \ohm \div 1\ \text{M}\ohm]$, usually we consider it $\simeq \infty$.
> 	- $Z_{out}$ : **output resistance**, $Z_{out} \in [100 \, \ohm \div\, 20 \ \text{k} \ohm]$, we usually consider it $\simeq 0$.
> - ***Open Loop Frequency Response Formula***:$$V_{out} = (V^{+}-V^{-})\cdot \frac{A_{DC}}{1+j\frac{f}{f_H}}$$Where:
> 	- $A_{DC}$ : open loop gain (ideally **infinite**, in reality $\in [10^5 \div 10^6]$).
> 	- $f_H$ : cut-off frequency $(f_H \in [1 \ \text{Hz} \div 1 \ \text{MHz}])$.

> A "real world amplifier" can be modelled by adding the "bias currents" ($I_{\text{bias}}$) and "input offset voltage" ($V_{io}$):<br>![[Pasted image 20240102191905.png|333]]
> - $V_{io} \in [\mu \text{V} \div \text{mV}]$
> - $I_{\text{bias}}$ : **input bias current**, $I_{\text{bias}} \in [\text{fA} \div \mu\text{A}]$ (**Remember**: $\text{f} = 10^{-15}$, $\mu = 10^{-6}$).

> Here are some circuits we have seen that use an operational amplifier:
> - [[SaM - Inverting Operational Amplifier]]
> - [[SaM - Non-Inverting Operational Amplifier]]
> - [[SaM - Charge Amplifier]]
> - [[SaM - AC-Coupled Amplifier]]
> - [[SaM - Differential Amplifier]]
> 	- [[SaM - Instrumentational Amplifier]]

---
###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_1.jpg]]

---

- ***Basic General Structure of an OP Amp (Operational Amplifier)***:<br>![[Pasted image 20231007111534.png]]
- ***Equivalent Circuit***:<br>![[Pasted image 20231007111611.png]]
	- Usually the resistances assume this values:
		- $Z_{in} \simeq \infty$
		- $Z_{out} \in [100 \, \ohm,\, 20k\ \ohm]$, we usually consider it $\simeq 0$
- ***Open Loop Frequency Response Formula***:$$V_{out} = (V_2-V_1)\cdot \frac{A_{DC}}{1+j\frac{f}{f_H}}$$Where:
	- $A_{DC}$ : Open Loop Gain, ideally **infinite**, in reality $\simeq [10^5 \div 10^6]$.
	- $f_H$ : Cut-Off Frequency, it can assume a wide range of values $\simeq [1 \text{Hz} \div 1 \text{MHz}]$.
- ***Bode Plot of the Open Loop Frequency Response***<br>![[Pasted image 20231007111841.png]]
