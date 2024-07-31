##### ***Remeber***:

> ![[Pasted image 20240123184928.png|333]]
> $$V_{out} = V_{in} \cdot -{R_2 \over R_1}$$

---
###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_1.jpg]]

---

- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAEMQ09xiURcALDz7cwSJkjDx4UWPAGlS0sIuIJiUZNJYAnTvnBg+gw3ypS4LAOb7uXW5xRCqkFgHcHYDIU9Go7-kghZmMg4X8PExVjbB9o-wAlU3BvEDxzVJcQAVpNF2gEFgAHfljw7DKUPG5sPOtSnyqaspMXFgAPcARJBAgvcwQhYL4E1k6nDTwkIiFq7PARlA6QDElCPl5wQiRhkAA1AEsAO2XsKvA8CGwEPjA8IYX9gHsAVwAXXWSvRoNvzQtXEA)<br>![[Pasted image 20231007121025.png]]
- ***Formula***:$$V_{out} = - V_{in}\frac{R_2}{R_1}$$
- ***Formula with $\beta$***:$$V_{out} = V_{in} \kern2px (1 - \beta)$$Where:$$\beta = \frac{R_1}{R_1 + R_2}$$And the formal definition of $\beta$, the **feedback factor** is:$$\beta \triangleq {V^{-} \over V_{out}}$$
- ***Formula with $A(f)$ and $\beta$***:$$V_{out} = V_{in} \cdot - {R_2 \over R_1}{A \beta \over 1 + A \beta }$$Where $A(f)$ is the **open-loop gain** of the amplifier, often defined as:$$A(f) = {A_{DC} \over 1 + j {f \over f_H}}$$And:$$V_{out} = A(f) \cdot (V^{+} - V^{-})$$
- **Sources**:
	- [[Op Amp Bandwidth.pdf|PDF]]
