##### ***Remeber***:

> #IMPORTANTE 
> We have seen the [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|resistive bridge]], let's see how the equations change when we consider a brige with 2 resistive sensors, instead of one:<br>![[Pasted image 20230611200647.png]]
> - We put the two sensors in "opposite sensing direction", so if we were to describe them we could say:$$\begin{array}{l}  R_1 = R_{10} \kern2px (1+x_1)  \\  R_2 = R_{20} \kern2px (1-x_2)  \end{array}$$
> - Then we define $R_3$ and $R_4$ such that the bridge is balanced, so we define the $K$-ratio:$$K = {R_4 \over R_{10}} = {R_3 \over R_{20}} $$
> - Finally if we calculate $V_0$ we will obtain:$$V_0 = V \left(\frac{1+x_1}{1+x_1+K} - \frac{1-x_2}{1-x_2+K}\right)$$If we consider $(1+K) \gg x_1$ and $(1+K) \gg x_2$, we can simplify the equation, resulting in:$$V_0 = V \cdot \frac{x_1+x_2}{1+K}$$Finally if $x_1 = - x_2$, so they both measure the same change:$$V_0 = V \cdot \frac{2 x}{1+K}$$

> #IMPORTANTE 
> It is called a half-bridge because if we perform the same calculation as before for "***Optimizing the Relative Sensitivity of the Bridge***", so:
> 1. Calculate:$$S(x) = \frac{1}{V}\frac{dV_{TH}}{dx}$$
> 2. Calculate $S(x=0)$, than calculate:$$\frac{dS(x=0)}{dK}$$
> 3. Find $K$ such that:$$\frac{dS(x=0)}{dK}=0$$
> 4. Find $K$ such that $S(x=0)$ is maximied, and we will obtain that for $K=1$ we will have $S_{MAX}$ and the final result will be:$$S|_{x=0 \kern2px _{MAX}} = \frac{1}{2}$$That's why it is called "**half**" brige.

> The [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|simple resistive bridge]] or ("$\frac{1}{4}$ brige") is called like that because if we perfom the same calculations we will obtain:$S|_{x=0 \kern2px _{MAX}} = \frac{1}{4}$.

> ***What are the gains of using a half bridge instead of a $1 \over 4$ brige?***
> - ==If $(1+K) \gg x_1$ and $(1+K) \gg x_2$ the half bridge behaves **linearly**==.
> - It has higher [[SaM - Sensitivity|sensitivity]]. #NOT_SURE_ABOUT_THIS (higher relative sensitivity perhaps, the sensitivity of the "quarter bridge" is not linear, so at specific points it might be higher that that of the "half bridge")
> - However it requires two sensors, so requires more space, and has a higher cost.

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_1.jpg]]

---
![[Pasted image 20230611200647.png]]

Define our two sensors:<br>![[Pasted image 20230611200704.png]]

Consider it a **balanced bridge**, so:<br>![[Pasted image 20230611200710.png]]

As usual, I consider the output $V_o$ and consider to work with **no load** (or an infinite load given by an ideal differential amplifier, infinite load ⇒ open ciruit) so I have the output which is equal to the open circuit differential voltage:<br>![[Pasted image 20230611200751.png]]

So we calculate $V_{TH}$ and we obtain:<br>![[Pasted image 20230611200827.png]]
- Notice how the two sensor oppose each other: $x_1-x_2$

This is easily fixed by inverting one of the two:<br>![[Pasted image 20230611200904.png]]

An half-bridge has some advantages with respect to the $\frac{1}{4}$ brige:<br>![[Pasted image 20230611200952.png]]

It is called a half-bridge because if we perform the same calculation as before for "***Optimizing the Relative Sensitivity of the Bridge***", so:
1. Calculate:$$S(x) = \frac{1}{V}\frac{dV_{TH}}{dx}$$
2. Calculate $S(x=0)$, than calculate:$$\frac{dS(x=0)}{dK}$$
3. Find $K$ such that:$$\frac{dS(x=0)}{dK}=0$$So $K$ such that $S(x=0)$ is maximied.

And we will obtain that for $K=1$ we will have $S_{MAX}$, such that:$$S|_{x=0 \kern2px _{MAX}} = \frac{1}{2}$$
The [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|simple resistive bridge]] or ("$\frac{1}{4}$ brige") is called like that because if we perfom the same calculations we will obtain:$S|_{x=0 \kern2px _{MAX}} = \frac{1}{4}$.