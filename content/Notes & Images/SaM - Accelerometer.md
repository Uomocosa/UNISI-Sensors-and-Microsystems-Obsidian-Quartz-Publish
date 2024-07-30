##### ***Remeber***:

> An accelerometer is just simple **mass-spring-dumper** system with two masses:<br>![[Lecture 4_230908_153707_2 1.jpg|500]]
> 
> We want to find the relation between the acceleration $\ddot x_s$ and the displacement $x_s$, such that by measuring the displacement we can measure the acceleration, so to calculate it we need:
> 1. Find the [[SaM - Lumped Parameter Systems|Lumped parameter system]] of this mechanical system (with the two masses):<br>![[Lecture 4_230908_153707_2 2.jpg|666]]
> 2. Find the [[SaM - Thevenim and Norton Equivalent|Thevenim Equivalent]]:<br>![[Lecture 4_230908_153707_4 1.jpg|500]]<br>Simplifying the **Thevenim resistance**, since $m_B \gg m_S$, so we exclude it from the load, since a parallel between $m_S \parallel m_B \simeq m_S$, also remember that $F_{ext} = m_B \cdot a$.
> 3. After applying the simplifications:$$H(s) = \frac{m_{\tiny{S}}}{m_{\tiny{S}}\cdot s + \lambda + {\huge{\frac{k}{s}}}}$$
> 4. Transform into [[Bode Plot|Bode form]], to finally obtain the [[SaM - Transfer Funtion of a Mounted Accelerometer|transfer function for a mounted accelerometer]]:$$\frac{R(s)}{A(s)} = \frac{m_{\tiny{S}}}{k} \frac{1}{{m_{\tiny{S}} \over k}s^2 + {\lambda \over k}s + 1}$$

> We can draw two graphs, the **Munted Behaviour** graph, and the **Unmounted Behaviour** graph:<br>![[Lecture 4_230908_153707_6 1.jpg|500]]
> - Where the first one (**Mounted Behaviour**, blue graph), assumes that $m_B \gg m_S$, so we can simplify the calculation.
> - While the second one  (**Unmounted Behaviour**, blue graph), does not make this assumption, and we have that: **the gain** $\left(A_{DC} = {m_s\over k}\right)$, the **natural frequancy** $\left(\omega_0\right)$ and **dumping ratio** $\left(\zeta\right)$ all depend on $m_B$, ==which is not good==, this means that every time you change the body on which the sensor is placed, you need to re-calibrate it.

---
###### Memory Card
![[Samsung_SaM_Notes_06_240515_120818_5.jpg]]

---
![[Lecture 4_230908_153707_2.jpg]]
![[Lecture 4_230908_153707_3.jpg]]
![[Lecture 4_230908_153707_4.jpg]]
![[Lecture 4_230908_153707_5.jpg]]
![[Lecture 4_230908_153707_6.jpg]]
![[Pasted image 20230710172105.png]]

==I have a **flat gain** and obviously that means that the operating range in the frequency domain is up to a maximum frequency $\omega_{MAX}$==

![[Pasted image 20230710172123.png]]
==The sensor has to be used mounted on a large object, otherwise the $A_{DC}$ will depend on the mass of the body ⇒ the sensor will have to be re-calibrated each time the change of the body sligtly changes (not good)==. 
