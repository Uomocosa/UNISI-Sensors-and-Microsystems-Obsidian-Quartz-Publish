##### ***Remeber***:

> ![[Pasted image 20240123184742.png|333]]
> $$V_{out} = V_{in} {1 \over \beta}$$Where:$$\beta = {R_1  \over R_1 + R_2}$$
---
###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_1.jpg]]

---

- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAEMQ09xiURcALDz7cwSJkjDx4IAdFKlpYBcQSrqU6SwBOnfODB9BBvlU2QWAcxPgMhEMXtg7UKCwDue0S642Ln42YjSCFlUw9+EOF+bCdeNwAlL2Tne18qKgFaVwzoBBYABxi4o1jOPG5sHKti8sqy4wydG1SUlzN4FgAPcAQqsAFicEJRBD5QvgTWHpRBkDwkIiEK2XBJlG7bRZQhsM5scbWQADUASwA7TYPRPAhsMfA8IQmTgHsAVwAXFiA)<br>![[Pasted image 20231007120747.png]]
- ***Formula***:$$V_{out} = V_{in} \left(1+\frac{R_2}{R_1}\right)$$
- ***Formula with $\beta$***:$$V_{out} = V_{in} \kern2px {1 \over \beta}$$Where:$$\beta = \frac{R_1}{R_1 + R_2}$$And the formal definition of $\beta$, the **feedback factor** is:$$\beta \triangleq {V^{-} \over V_{out}}$$
- ***Formula with $A(f)$ and $\beta$***:$$V_{out} = V_{in} \cdot{A  \over 1 + A \beta }$$Where $A(f)$ is the **open-loop gain** of the amplifier, often defined as:$$A(f) = {A_{DC} \over 1 + j {f \over f_H}}$$And:$$V_{out} = A(f) \cdot (V^{+} - V^{-})$$
- **Sources**:
	- [[Op Amp Bandwidth.pdf|PDF]]