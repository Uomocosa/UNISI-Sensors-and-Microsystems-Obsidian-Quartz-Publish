# Index
- [[#ODE Description of a Second Order System]]
- [[#Definition of $A(s)$, $I(s)$, $H(s)$, $A_{DC}$, $ zeta$, $ omega_0$]]
- [[#Dynamic Behaviour of a Second Order System (Modes of Poles)]]
- [[#Frequency Analysis of Complex Poles for Second Order System]]

---
Okay at this point we can go and discuss and recall what happens for a second order system. 

###### ODE Description of a Second Order System
![[Pasted image 20230707112605.png]]
So we take a second order system by writing a **second order dynamic model**. 
So we start from the ODE which is the ordinary differential equation which represents this kind of systems, in time domain: $e(t) + \cdots$
And I take the simple model where I consider to have this term equal to $0$.
I don't have any zeros in the transfer function. 
Okay so we restrict the study to this simple model we go to the Laplace domain. 
So I can write: $E(s) \cdots$
And I take this polynomial here: $E(s) = G(s) \cdots$
%%So then you start:%%

---

###### Definition of $A(s)$, $I(s)$, $H(s)$, $A_{DC}$, $\zeta$, $\omega_0$
==Then you define two polynomials: $A(s)$ which defines the pole of the system, and $I(s)$a polynomial depending on the initial conditions==.
So we can write $H(s)$:
![[Pasted image 20230707112617.png]]
==$H(s)$ is a transfer function, which gives me the ratio between the output and the input==, when the initial condition is (a step function):
So we have the dynamic of the system which is defined by 3 parameters:
![[Pasted image 20230707112638.png]]
1. $A_{DC}$ Gain in DC (Direct Current, meaning at low frequency)
2. $\zeta$ : damping ratio, also defined by $Q$ (the $Q$ factor)
3. $\omega_0$ : natural frequency

%%So essentially $a_2$ for the dynamics $A_1$ for the gain or in body form these 2 parameters here and %%
We have that $\zeta$ is the damping ratio, ==an alternative way to express these behavior here is the $Q$ factor which essentially describes the stored energy or power divided by the dissipated energy==. 
And then we have $\omega_0$ which is the natural frequency. 
Obviously we have that $\zeta$ is: ...
Okay, the two poles $p_1$, $p_2$, are: ...

---

###### Dynamic Behaviour of a Second Order System (Modes of Poles)

![[Pasted image 20230707112651.png]]
So we have obviously two cases which result into a different dynamic behavior. 
==The first is if this parameter damping ratio is larger than $1$ (so if $\zeta > 1$), and in this case the two poles belongs to the real numbers and in this case we can write for instance the response to the initial conditions of the system, in this way==: $e(t) = \cdots$
Actually this is here you see you have cause hyperbolic cosine which actually means that this function here is a combination of the two exponential functions: $x_1(t) = \cdots$ and $x_2(t) = \cdots$
And this two parameter $\tau_1$ and $\tau_2$ are simply: ...
So actually even if this formula here gives an expression which resembles the sum of cosine and sine it's a dipol function so they are obtained by combining the exponential functions with two exponential functions.
Obviously in case of response to a step function we have a behavior which is the similar:
![[Pasted image 20230707112702.png]]

And then same as before, I'm going forward and I write it:
![[Pasted image 20230707112716.png]]
%%So I'm going to start with sine of the same thing. %%
==This is what happens if we have the opposite situation that is where $\zeta < 1$: so $p_1$, $p_2$ belongs to the **complex numbers**== and we can write them this way: ...
So in that case we have the response to that initial condition: $e(t) =\cdots$
%%As far we can also write this way which maybe it's not simple. %%
Where $\varphi$ is the inverse tangent of ... 
Obviously all these responsible initial condition I have written are under the assumption of having the first derivative initial condition equal to $0$ (when defining the 2 order model we have supposed $b_1\kern2px g'(t) =0$), which I have to take in account.
So we have the resposne to a step funciton, as usual:
![[Pasted image 20230707112730.png]]
$\varphi$ is the same, defined before. 
What we can say here we see that we have a decay of these transient response here ($e^{-\zeta \omega_0 t}$). 
The steady state is represented by this one here:
So the **equivalent time constant** is: $\tau_{eq} = \cdots$
We can also also express it in terms of $Q$, is the same: ...
So for instance and at the end, we can write: ...
$T_0$ is the period of the natural frequency. 
==Actually you see that the frequency of the transient response this part here is not exactly the natural frequency, we have this modal frequency which is given by this one, nd this is tell us how long is the time needed for the transient to vanish==:
![[Pasted image 20230707112742.png]]
So we can think about the rule of thumb which is also the number of periods you have of the natural frequency you have to wait before the transient vanishes. 
So obviously this corresponds to having this value here, this time this is $e$ and length of this transient here is described by this parameter.
Whereas this is given by something which resembles this frequency here.

---
###### Frequency Analysis of Complex Poles for Second Order System

Now we go to the **frequency domain**, in case of **two complex poles**:
![[Pasted image 20230707112759.png]]
We put here $\omega$ and here this, we start from $A_{DC}$.
==We have two zeros so this is a **DC coupled system**.==
So we have a peak which is at a radian frequency close to $\omega_0$, and this is the exact frequency of the peak, obviously if $\zeta^2$ this larger than $1 \over 2$ that means that: $Q < \frac{1}{2}$
Which corresponds to: $\omega_p = \cdots$
Then this peak is not more present.
So no resonant frequency.
==So this peak here and this frequency exists only if we have this condition satisfied==: $\zeta < \frac{1}{\sqrt{2}}$
![[Pasted image 20230707112826.png]]
The name of the peak is "**resonant frequency**", is the maximum response to an input.
But this frequency here we have the maximum possible response to a harmonic input. 
And so if I draw this two curves: 
