- ***Source***: [Internet Page](https://lpsa.swarthmore.edu/Bode/BodeReviewRules.html) | [[Rules for Drawing Bode Diagrams 1.pdf|Downladed PDF]]
- ***Amplitude***:
	- **Real zero**: $+20 * \text{zero's multiplicity} \kern3px {\text{dB}\over\text{decade}}$
	- **Real pole**: $-20 * \text{pole's multiplicity} \kern3px {\text{dB}\over\text{decade}}$
	- **Imaginary zero**:
		- $+40 * \text{zero's multiplicity} \kern3px {\text{dB}\over\text{decade}}$
		- Peak at $w = w_0 \sqrt{1 - 2 \zeta^2}$
	- **Imaginary pole**:
		- $-40 * \text{pole's multiplicity} \kern3px {\text{dB}\over\text{decade}}$
		- Peak at $w = w_0 \sqrt{1 - 2 \zeta^2}$

- ***Phase***:
	- **Starting Phase***:
		- $+0°$ if $K \gt 0$ ($K$ is the gain)
		- $\pm180°$ if $K \lt 0$ ($K$ is the gain)
	- **Real zero**: $+90° * \text{zero's multiplicity}$
	- **Real pole**: $-90° * \text{zero's multiplicity}$
	- **Imaginary zero**: $+180° * \text{zero's multiplicity}$
	- **Imaginary pole**: $-180° * \text{pole's multiplicity}$

- ***Frequency Domain Response (Bode Form)***:
	- For a single-pole system, the transfer function in frequency domain is represented as: $H(j\omega) = \frac{A\_{DC}}{1 + j\frac{\omega}{\omega\_T}}$, where $A_{DC}$ is the DC gain and $\omega_T$ is the cutoff frequency.
	- Cutoff frequency ($f_T$) or $-3 , \text{dB}$ frequency is related to the time constant $\tau$ as: $\omega_T = \frac{1}{\tau}$.

- ***Bode Plots***:
	-  The module of $H(j\omega)$ is represented in dB as $20 \log |H(j\omega)|$.
	- The DC gain ($A_{DC}$) is the value of $H(j\omega)$ when $\omega = 0$.
	- The cutoff frequency ($f_T$) corresponds to $|H(j\omega_T)| = \frac{1}{\sqrt{2}}$ in dB.

---
#### Gain
- A **real zero** means $+20 \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
- A **real pole** means $-20 \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
- An **imaginary zero** 
	- means $+40 \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
	- In the case of an imaginary zero there is a also peak is at  $w = w_0 \sqrt{1 - 2 \kern2px \zeta^2}$
- An **imaginary pole**:
	- means $+40 \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
	- There is a also peak is at  $w = w_0 \sqrt{1 - 2 \kern2px \zeta^2}$
	- ~Ex.:<br>![[Pasted image 20230418162842.png]]

----
#### Phase
- **Starting Phase***:
	- $+0°$ if $K \gt 0$ ($K$ is the gain)
	- $\pm180°$ if $K \lt 0$ ($K$ is the gain)
- **Real zero**: $+90° \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
- **Real pole**: $-90° \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
- **Couple of conjugate complex zero**: $+180° \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**
- **Couple of conjugate complex pole**: $-180° \cdot \mu \kern5px \frac{\text{dB}}{\text{dec}}$, where $\mu$ is its **multiplicity**

---
