In an [[SaM - Operational Amplifier|operational amplifier]] we need to consider an **input offset** $\left(V_{io}\right)$ and two **bias currents** $\left(I_{b1},\ I_{b2}\right)$, we can model it like this:<br>![[Pasted image 20240116185406.png|500]]

---
We can then model the whole measurement system, by adding the [[SaM - Thevenim and Norton Equivalent|Thevenim equivalent]] of the measurement system as the input to the amplifier:<br>![[Pasted image 20240116185532.png|500]]

---
If we wish to know the effect of the **non-idealities** of the amplifier on the output we can calculate $\left.V_{out}\right|_{\large{V_s=0}}$ and the result is: #IMPORTANTE $$\left.V_{out}\right|_{\large{V_s=0}} = \left(1 + {R_2 \over R_1} \right)\left(I_{b2} R_S - I_{b1}{R_1 R_2 \over R_1 + R_2} + V_{io} \right)$$And this is called **OZE**: *Out of Zero Error*.

While we can also define the **IZE**: *Input out of Zero Error*:$$\text{IZE} = I_{b2} R_S - I_{b1}{R_1 R_2 \over R_1 + R_2} + V_{io}$$Even if the source $V_S = 0$, since the amplifier is not ideal, we will measure an ouput like if $V_S = \text{IZE}$ and an having [[SaM - Operational Amplifier|ideal operational amplifier]].

---
By having an **OZE** we have a non-symmetrical **dynamic range**:<br>![[Pasted image 20240116190337.png|500]]
Ideally we want no **OZE** and a $0 \ \text{V}$ output if the input is $0 \ \text{V}$.
Instead we have $V_{out} = \text{OZE}$ for $V_S = 0 \ \text{V}$.
==However if the **OZE** is **constant**, this is not a big problem, since it can be corrected==.

---
The real problem is that the **OZE** is not constant, instead it has a **drift**, due to envirement condition, aging, temperature, ..., and this variation cannot be corrected :<br>![[Pasted image 20240116190630.png]]
(green/blue line: real **OZE**)
(red line : previously calculated **OZE**)

---
For this reason, if we want a **high [[SaM - Accuracy or Maximum Error|accuracy]]** we need to select a special kind of amplifier, called =="***precision amplifier***"==.
These devices are often **low freqeuncy** device (or "**narrow bandwidth** devices", it means the same thing), but with **really low DC errors**.

We can find different classes of **precision amplifeirs**: #IMPORTANTE 
1. **Low input bias current op. amp.** with $I_{b} \lt 100 \ \text{pA}$.
2. **Precision amplifiers** with $V_{io} \lt  1 \ \text{mV}$ (can also be found with $V_{io}$ in the range of $\sim \mu \text{V}$) and with a $\text{TCV} \lt 2 {\mu \text{V} \over ° \text{C}}$ (*Temperature Coefficicent of Voltage*, similar to the [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|TCR]]).
3. **Zero drift op. amp.** $V_{io} \sim  5 \ \mu\text{V}$, $\text{TCV} \lt 2 {\text{nV} \over ° \text{C}}$, however these are **slow devices**, so a high [[SaM - Rise Time|rise time]] (or "limited **slew rate**") and also have a really **narrow band**.
4. **Low noise amplifier**: they minimize the white noise interferance and not the DC offset.<br>Here's how we can model the input-noise in an amplifier:<br>![[Pasted image 20240116192422.png]]

Here's a table to better rember them:

|                                  | $I_b$             | $V_{io}$                                            | **TCV**                                             | Other                                                  |
| -------------------------------- | ----------------- | --------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------ |
| *Low input bias current op.amp.* | $<100\ \text{pA}$ |                                                     |                                                     |                                                        |
| *Precision amplifiers*           |                   | $< 1 \ \text{mV}$                                   | $\lt 2 {\mu \text{V} \over ° \text{C}}$             |                                                        |
| *Zero drift op. amp*             |                   | $\sim 1000$ times lower then *precision amplifiers* | $\sim 1000$ times lower then *precision amplifiers* | **Slow devices** (high [[SaM - Rise Time\|rise time]]) |
| *Low noise amplifier*            |                   |                                                     |                                                     | Minimize the white noise interferance.                 |

As a rule of thumb we can also say that generarly the **drift offset** can be considered equal to:  #IMPORTANTE $$V_{\small{\text{DRIFT}}} = {1 \over 10} V_{io}$$$V_{io}$ (the input offset of the amplifer) is given by the manifacturer in the data-sheet.

---
So to summarize for **DC measurement** we have that: #IMPORTANTE 
- **DC offset**: can be corrected
- **Drift offset** (variable offset): cannot be corrected.
- $V_{\small{\text{DRIFT}}} = {1 \over 10} V_{io}$.

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_3.jpg]]
![[Samsung_SaM_Notes_21_240516_160358_4.jpg]]

---