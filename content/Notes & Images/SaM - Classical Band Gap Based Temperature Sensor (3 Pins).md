##### ***Remeber***:

> To understand this circuit you need to rememebr:
> - How [[SaM - Current Mirror|current mirror]] is made.
> - The [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT formula (in active region)]].

> Also let's see how many BJT in parallel behave, this is the circuit:<br>![[Pasted image 20240116121217.png|250]]
> The current $I_C$, will be the sum of all the currents of each parallel BJT.<br>we consisder them equal and define the currents of each parallel BJT as "$I_{C_2}$", so we have:$$I_C = N \cdot  I_{C_2}$$This is like having a **more conducting device**, where the current is $N$ times the current of the single the basic device, so if we use the [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT formula]], we can say:$$I_C = NI_{S_2} \kern2px e^{\frac{q V_G}{KT}}$$

> This is the strucuture of a "***classical band gap based temperature sensor***":<br>![[Pasted image 20230719123740 1.png|500]]
> - We have a differential structure with two identical resistances, and two different BJT.
> - The 2nd BJT is the strucutre we have seen before with $N$ parallel BJT.
> - The bases of the BJT **(1)** and **(2)** are at the same voltage, and the circuit here is concluded with a **feedback loop**.
> - This is an **amplifier** which has a **very high gain**.<br>⇒ Therefore these two voltages, $V_{-}$ and $V_{+}$ are approximately at the same value.
> - So **(1)** and **(2)** have also the the same collector voltage.
> - Since the two resistances $R_C$ are nominally identical we have the same current in these two branches here ($I_C$).
> - Here's a [circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKABdwU8Rs1xCqvKlQgMALNFIJiYMRjGEEKBWHIw4Y-GDwZCYQrgQI8YpGDggAJnQBmAQwCuAGzbtwunnzTchUcCHFJYmlZeUVlPTVYSE08bV19Q2NTZCpre2dXDhRlTyoUBEI8v1EJKRk5BSUVKI0tHT0DSCMTMwt0xxc3PEE+ZhRikQCy4Iqw6sioaNj4xqTW1KtbTqzPYsIxQf9A8tCqiNUpuriGxObktrTlzJYAdxAczd9VIt9IO-dXvq5Bj7Af3w9X73IG+XjAkAbHgxcD-aGbd73frw-iCGGI1Eo7wojHY3CbAqvdEfQk8bBFPHkqAk-Bkor6QRUjEMumwgbYJl-OEcopQnnU+6k-EPQoioq40X8oWEbjvDhifTFbAmLalIIhOQ6bC6DYQdQxfAoMBCLg5ZiEenta5dABOYvtpLAxAGIngLDtyoJkpVTpdqQl9OdxV94A+zyDnvAQdYACVgxG+mIEX5NNRhFMECTRaSFF7xSw7CBcw8MAMlNxMANuGAkExLvAqCNSM2xHhiNgxMQSEWgs3SG2MHgSO3-XAPuWS2WAXwMQqvrRp8IPnPio8IZH+RuZdS7dKK6KxODXW77lufCrDy6wyqhTe8LLrwT7zwVcKMZGuNxi5+BfbLy-Nn-d8L3BYt-xQd0-3BHMuxKBt3gAcz-WDSQQOEl3uFdfCw7dZ0Vckv1BbcIKAA). (Circuit at rest $I_S = 100 \ \text{fA}$, BjTs **NOT in active region**):<br>![[Pasted image 20240116131251.png|500]]
> - Her's another [circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKGxRAGEALAQwDsA5nQA6AZwDKvAC4BXAE4yAlgHt+4zgvl1+0qOEZgqx8NCQmOECCdZ6wKPCHZUwhKs-0QG2aHmKRiPAAWMGJsLAxiBHNoFGxsMDxCDCC8bEISP0xkKh4BYXEpOUVpVXUxTXltXRY7DEInNBA0Rw8XEG9ff0CQsIiomLiEpJS0jMDibKNcviFRSRkFZTUNLR1pWuaUIMaqFAQGtvAOnz8A4NDwrAGoWPjE5NT0zMnyaa5ZgoXi5fLK6o2ejw7iazA4Ry8p26Fz612ityGD1GzwmUzgH3y8yKS1KKwqaxqenYuxAhB2EJOXXOvSukXhqHuIye4yyb3ReTmhUWJTKqyq6xYAHctuTQfUSZAheBxR57K0mpLhXKScCJVLVR5iW0pWSnJAdmC9TtFeB7EbwG5zSbXO59c18FapS1zftDnaTa6nOl7a1vR6HfEGjavQ1rZbA6bwX6pYaI7qIx6Di6k57E4dvZ70o5JXoQocmthghLjp0zqQENtMMCyFgESlRpBsMQMghmEFmzkMZzvjjefj+TV5M0UyOg5NPPAWEPCztM0XQhwXJPhZ6FyS16xhbLxzPwOPWAAldc70FBY36IK0fTGMxO0cgIK61MsXgPp8YDgVxyYDiOMBIJgkGmeAqCCaByzwYJ2zcPBW3IMCIIGIJKEgjcQJNL9mg-CgHDVYU8xJTDtXw1wSRQbY8KcIsI13LMoCnYdDkIb8kyCYkl2XKjyWYriH3YqVdznWdIPorciwcVpqPdATxJEx9hOzO8GjY8EixU0TePU+S+I4FAGM9dSDI7DjJ0ERiHw7T1W0XDSCI8OyeJNBzHFSdweL0oA) (Go to one of the BjT in the circuit `>>` Double click it `>>` "Edit Model" `>>` Change the value of the "*Saturation Current*", and see how the output voltage change.)<br>Here's it with each BjT at $I_S = 100 \ \text{pA}$, and they are in **active region**:<br>![[Pasted image 20240116131217.png|500]]

> Because you know that both BJT are in the **active region** ⇒ **we can neglect the base current**, so $I_C \simeq I_E$.
> So now we can relate the $I_C$ current to this voltage $\Delta V_{BE}$:$$  \Delta V_{BE} = V_{BE_1} - V_{BE_2} = I_C \kern2px R_T $$And since we know that a [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT in active region]] has this formula:$$V_{BE} = \frac{kT}{q}\ln\left({I_C \over I_S}\right) $$And the property of logaritms $\ln(a) - \ln(b) = \ln(\frac{a}{b})$, we can say:$$\Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{I_C}{I_{S_1}}\frac{I_{S_2}}{I_C}\right)$$We simplify:$$V_{out} = \Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{I_{S_2}}{I_{S_1}}\right)$$Note that the ratio between $I_{S_1}$ and ${I_{S_2}}$ is equal to $\frac{K_2}{K_1}$, we can also say that:$$V_{out} = \Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{K_2}{K_1}\right)$$

> We know that: 
> - $V_{out} = \Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{I_{S_2}}{I_{S_1}}\right)$
> - $I_C = N I_{C_2} = NI_{S_2} \kern2px e^{\frac{q V_G}{KT}}$
> - $I_C = I_{C_1} = I_{S_1} \kern2px e^{\frac{q V_G}{KT}}$
> - $I_C = {\Delta V_{BE} \over R_T}$
> - $V_{out} = I_C R_T$
> 
> So:$$\frac{I_{S_2}}{I_{S_1}} = \frac{1}{N}$$And we can finally calculate the function of this sensor: #IMPORTANTE $$V_{out} = R_T {k T \over q R_1} \ln (N)$$It has a **linear dependance on temperature**.

> The usual values for the [[SaM - Sensitivity|sensitivity]] for this kind of devices are in the range: #IMPORTANTE $$\alpha \in \left[2 \ {\text{mV}\over°\text{C}}\div 10 \ {\text{mV}\over°\text{C}}\right]  $$

> So this device that we have here, we have discussed is a device with three pins:<br>![[Pasted image 20230719123826.png]]
> - In the theory we have found no offset, but in reality there could be one.
> - So this is a **3 pin device**, but there also exists other circuits based on the same philosophy and the same topology or similar topology which instead have **2 pins**.

---
###### Memory Card
![[Samsung_SaM_Notes_25_240516_113814_2.jpg]]

---
This is the structure that can be used also to obtain regulated voltages where the temperature dependence is compensated (or eliminated).
![[Pasted image 20230719123740.png]]
- We have a differential structure with two identical resistances, and two different BJT.
- The 2nd BJT can be seen more clearly (how it is strucutered) on the right.<br>it's like having many BJT in parallel.<br>⇒ This means that the current here $I_C$, will be the sum of all these currents, of each parallel BJT.<br>This is like having a **more conducting device**, where the current is $N$ times the current of the single the basic device.
- The bases of the BJT **(1)** and **(2)** are at the same voltage, and the circuit here is concluded with a **feedback loop**.
- This is an **amplifier** which has a **very high gain**.<br>⇒ Therefore these two voltages, $V_{-}$ and $V_{+}$ are approximately at the same value.
- So **(1)** and **(2)** have also the the same collector voltage.
- Since the two resistances $R_C$ are nominally identical we have the same current in these two branches here ($I_C$).

Because you know that both BJT are in the **active region** ⇒ **we can neglect the base current**, so $I_C \simeq I_E$.
So now we can relate the $I_C$ current to this voltage $\Delta V_{BE}$:
![[Pasted image 20230719123800.png]]

And so we have the output voltage here:
![[Pasted image 20230719123754.png]]
- We use the property of logarithms: $\ln(a) - \ln(b) = \ln(\frac{a}{b})$
- So we have: $\Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{I_C}{I_{S_1}}\frac{I_{S_2}}{I_C}\right)$
- We can simplify $I_C$ and obtain:$V_{out} = \Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{I_{S_2}}{I_{S_1}}\right)$
- Where there ratio between $I_{S_1}$ and ${I_{S_2}}$ is equal to $\frac{K_2}{K_1}$.
- So finally: $$V_{out} = \Delta V_{BE} = \frac{KT}{q}\ln\left(\frac{K_2}{K_1}\right)$$
- We have supposed that the ratio $\frac{K_2}{K_1}=10$ but this depend on the structure, since we have that:$$I_C = I_S \kern2px e^{\frac{q V_G}{KT}}$$Then we wil have that since both $I_C$ are equal and $I_{C_2}$ is the sum of $N$ identical collector currents (since the 2nd BJT is the parallel of many BJT):
	- $I_C = I_{C_1} = I_{S_1} \kern2px e^{\frac{q V_G}{KT}}$
	- $I_C = N I_{C_2} = NI_{S_2} \kern2px e^{\frac{q V_G}{KT}}$
	- So finally we have: $$\frac{I_{S_2}}{I_{S_1}} = \frac{1}{N}$$There must be an error somewhere becouse in this case the output comes out as negative with respect to what there is written in the notes, since:<br>$\ln\left(\frac{1}{N}\right) = - \ln(N)$<br>This is not a big problem, but it is different.
- So in this particular example we have supposed $N=10$, so the BJT **(2)** is composed of 10 stacked BJT.
- **NOTE**: If we choose to stack only 1 BJT, so $N = 1$, we have that $\ln(1)=0$ so we need at least $2$ BJT in parallel in position **(2)**, to have a reading.

![[Pasted image 20230719123814.png]]
- So now $V_{out}$ has a **linear realtionship with temperature**, really good, this means that is also has a **fixed sensitivity** $\alpha$.
- **NOTE**: We have supposed a $V_{ref}$ **independent on temperature**. 

So this device that we have here, we have discussed is a device with three pins.
![[Pasted image 20230719123826.png]]
- In the theory we have found no offset, but in reality there could be one.
- So this is a **3 pin device**, but there also exists other circuits based on the same philosophy and the same topology or similar topology which instead have **2 pins**.
