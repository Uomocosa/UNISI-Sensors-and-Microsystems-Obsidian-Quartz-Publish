##### ***Remeber***:

> Now we will see the plot for a **high-pass filter**:<br>![[Pasted image 20230707112514.png]]

> There is no response to static input to a continuous input. In fact $H(0)$ is equal to $0$.
> That means that lean means for $s$ which goes to $0$ then $H(s)$ divided by $s$ is equal to:<br>![[Pasted image 20230707112538.png]]
> - So for sure we don't have any response to a continuous input. 

> ==**AC Coupled System**:<br>Only the alternating part (depending on $\omega$) passes trhough the system, **there is no continuous input**==.

> ![[Pasted image 20230707112553.png]]
> For the real behavior, obviously we don't have any real system which behaves as the system here, because at the end all systems have an output which goes to zero with infinte frequency (we draw the real behaviour as the dotted line), so **this is an approximation of a real system** which holds for some simple devices, like for instance, the most simple one I have mind is the **high pass filter**. 
> So this is very simple high pass filter.

> So obviously this is an approximation because at the end the **parasitic capacitance** will play a role and so we will have something different from this many other effects at the end for sure, we will not see again an infinite frequency which is a constant it will go to zero. 
> So here we are simply neglecting the poles which have higher frequency and looking at the most relevant behavior of the system which is the one that can be described by this simple system (also this process or simplification is known as "**dominant poles**"). 

---
###### Memory Card
![[Samsung_SaM_Notes_01_240516_165350.jpg]]

---
Start:
![[Pasted image 20230624220947.png]]
- ==**NOTE**: The first term should be $\dot e(t)$.==

Laplace domain: <br>![[Pasted image 20230624221011.png]]
![[Pasted image 20230624221036.png]]
If we consider the response to a step input:<br>![[Pasted image 20230624221120.png]]
We can write this:<br>![[Pasted image 20230624221151.png]]
$\ldots$
$\ldots$
Here you have the respons to initial conditions:<br>![[Pasted image 20230624221454.png]]
Here you have the response to the input:<br>![[Pasted image 20230624221506.png]]

Response to the input:
![[Pasted image 20230624221623.png]]

Response to initial conditions:
![[Pasted image 20230624221653.png]]

Super-imposition of the two:
![[Pasted image 20230624221719.png]]
==So from now, I know that when I suddenly change the input of the first order system, 
I must wait for a time given by approximately **five times the time constant of the system** before reaching the steady state condition==. 
==And also I know that the so-called **DC gain** is given exactly by the sensitivity of the system **in static condition**==. 