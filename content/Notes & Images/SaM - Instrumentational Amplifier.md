###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_2.jpg]]

---
- ***Online Resource***: [Wikipedia](https://en.wikipedia.org/wiki/Instrumentation_amplifier)<br>![[Pasted image 20231004153316.png]]
- Formula:$$V_{out} = (V_2 - V_1)\cdot\left(1+\frac{2R_1}{{R_{\text{gain}}}}\right)\frac{R_3}{R_2}$$
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENwAWTkbBFECk5U+AvOCRMkYePEGxZpUrOzkBM2ey49mAoVV0hiEkFOSyqnaEuJo4YEqQSFqG+CwBK2oy+K+XVJa0UCEwCJ7e2ITifrzRoSDCgglhLABOgkmG+uC2IW7pmQZ5OZgCBu4ZpRh6SaL57gDukVHeZVAszWDcgjVFveWd3mAo4t06eZBD47m1xYNVWSO8aODLFXCFOfXYq-UbU827BsvHgvgdHGcoQokOgrdjkmDSFlQMMJykeITwhNhfLBgcQfaBfJzwYHgzijcyVXitQyce6GA5DbCI06rVFDZEuJH3G48Q53FxExKccTkknXOp7fgdI70gQYlz7Qqs3gMvFc8pwlgAc1JvOF2DwxI6AAcKVTbtxxLgeNhQoKZbxIDx5bxxSqgA) (with numerical values): <br>![[Pasted image 20231004153201.png]]
- ***Why should I use an Instrumentational Amplifier instead of a [[SaM - Simple Differential Amplifier (Made from an O.A.)|Simpler Differential Amplifier]]?***
	- The IA typically has a higher input impedance compared to a simple Differential Amplifier, since the inputs are feed directly to other operational amplifier.
	- It has a [[SaM - Definition of CMRR (Common Mode Rejection Ratio)|Better Common-Mode Rejection Ratio (CMRR)]]
	- Also the Instrumentation Amplifiers often offer the flexibility to adjust the gain to suit specific application requirements.

---

- ***Online Resource***: [Wikipedia](https://en.wikipedia.org/wiki/Instrumentation_amplifier)<br>![[Pasted image 20231004153316.png]]
- Formula:$$V_{out} = (V_2 - V_1)\cdot\left(1+\frac{2R_1}{{R_{\text{gain}}}}\right)\frac{R_3}{R_2}$$
- Following my own calculations:$$\left.\frac{V_{out}}{V_1}\right|_{V_2=0} = -\frac{R_1}{R_{\text{gain}}}\cdot\left(\frac{R_3}{R_2+R_3} \frac{R_2+R_3}{R_2}\right) - \left(\frac{R_1}{R_{\text{gain}}}+1\right)\cdot\frac{R_3}{R_2}$$And:$$\left.\frac{V_{out}}{V_2}\right|_{V_2=0} = \left(\frac{R_1}{R_{\text{gain}}}+1\right)\cdot\left(\frac{R_3}{R_2+R_3} \frac{R_2+R_3}{R_2}\right) + \frac{R_1}{R_{\text{gain}}}\cdot\frac{R_3}{R_2}$$So we can say:$$V_{out} = \left[{2R_1 \over R_{\text{gain}} + 1}{R_3 \over R_2}\right]V_2 - \left[{2R_1 \over R_{\text{gain}} + 1}{R_3 \over R_2}\right]V_1$$So:$$V_{out} = {2R_1 \over R_{\text{gain}} + 1}{R_3 \over R_2}(V_2-V_1)$$
---
