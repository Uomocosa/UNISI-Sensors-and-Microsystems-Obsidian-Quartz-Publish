###### Memory Card
![[Samsung_SaM_Notes_01_240516_165350.jpg]]

---
ODE (**Ordinary Differential Equation**) : 
$$e(t) + a_1 e'(t) + a_2 e''(t) + \ldots = b_0g(t) + b_1g'(t) + \ldots$$
⇒ **Laplace Domain**: 
$$\begin{align}&E(s) \kern2px + \\ & a_1sE(s) - a_1e(0^-) \kern2px + \\ & a_2s^2E(s) - a_2se(0^-)- a_2e'(0^-) = \\ &b_0G(s) \kern2px + \\ &b_1sG(s) - b_1g(0^-)\end{align}$$
⇒ Polynomials $A(s)$ (of $p$ order) and $B(s)$ (of $z$ order): 
![[Pasted image 20230624210905.png]]
![[Pasted image 20230624210951.png]]

And then I define also a polynomial $I(s)$ which accounts for all the times related to initial condition:<br>![[Pasted image 20230624211113.png]]![[Pasted image 20230624211133.png]]

Important:
![[Pasted image 20230624211459.png]]

Therefore, if I have no initial condition, I'll have this response here:<br>![[Pasted image 20230624211512.png]]

==You know very well that for real linear system, the pole of this response are all stable==:<br>![[Pasted image 20230624211610.png]]
==The pole of the system, $A(s)$ has stable zeros==.
==That means that the function $H(s)$, which is called **transfer function** we found **has stable poles**==.
And we write again:<br>![[Pasted image 20230624211630.png]]
==So this eqaution has stable poles as well, and the poles are the same because we have the same polynomial at the denominator, $A(s)$==. 
==So the dynamics of the initial condition and of the transient part of the response to the input is the same==. 
