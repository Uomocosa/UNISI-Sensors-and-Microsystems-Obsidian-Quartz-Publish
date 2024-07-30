##### ***Remeber***:

> 1. ***Set the output range*** $V_{TH_{MAX}}$, from this find $x_{\max}$.
> 2. ***Check the power ([[SaM - Self-Heating|self heating]])***:$$P = \left(V \over R_1 + R_4\right)^2 \cdot R_1$$
> 3. ***Check [[SaM - Accuracy or Maximum Error|accuracy or maximum error]]***:$$\Delta V_{TH} \approx {dV_{TH} \over dx}\Delta x \gt \text{Noise level, IZE (Amplifier), drifts}$$
> 4. ***Linearity of the bridge***: so if $1 + K \gg x$.<br>The [[SaM - Non-Linearity Error|non-linearity error]]:$$\text{NL} = \frac{x}{1+K}$$So assert that:$$\text{NL}_{\text{accettable}} \gt \frac{x_{\max}}{1+K}$$
> 
> 

---

Follow this 3 steps:
![[Pasted image 20230611191006.png]]
![[Pasted image 20230611191057.png]]
![[Pasted image 20230611191227.png]]

And if we measure it in a certain condition, which is around $x = 0$, it will give us this expression here:
![[Pasted image 20230611191348.png]]

![[Pasted image 20230611191815.png]]

So in fact, if I draw what happens here, I will have this:<br>![[Pasted image 20230611191833.png]]
- Different lines correspond to different values of $K$.

==I will have an $X^{K}_{\text{LIN}_\text{MAX}}$ , which stands for the maximum value for $X$ (given a certain $K$), under which we are in the **linear region**==.
![[Pasted image 20230611191855.png]]

So for me, "**ideal linear**" is a circuit where I would have exactly this output here:<br>![[Pasted image 20230611191951.png]]
- Not as an approximation, but as a real output.

Then I evaluate the non-linearity in this way:<br>![[Pasted image 20230611192009.png]]

Where:
![[Pasted image 20230611192048.png]]
- $V_{TH_{ID}}$ is the **linear approximation** we make when we are in the linear region (straigth lines), and we can write: $$V_{TH_{ID}}(x) = \frac{K}{(1+K)^2}x$$
- $V_{TH}$ is the real line: $$V_{TH_{}}(x) = \frac{K}{(1+K)}\frac{x}{(1+K+x)}$$
- So we have that the $NL$ (non-linear error) is equal to:$$\text{NL} = \frac{x}{1+K}$$

![[Pasted image 20230611192138.png]]
- Given your maximum value of $x$, so the **range of your measurement** of our sensor ($R_1$), you will find the right value for $K$. 

For instance, if I have $1\%$ as possible acceptable non-linearity, then I will have that key has to be approximately $100$ multiplied by the maximum value of $X$, which is your measurement range:<br>![[Pasted image 20230611192257.png]]


The last point of the design of the bridge is point 5. ***Optimizing the Relative Sensitivity of the Bridge***:
![[Pasted image 20230611195950.png]]
- Remember:  $x$: "*deviation output of the sensor*"

![[Pasted image 20230611200028.png]]
![[Pasted image 20230611200139.png]]

This means that the maximum sensitivity it's reached if $K$ :<br>![[Pasted image 20230611200217.png]]

So this means that you optimize the bridge for the point of view of the sensitivity is the one in which all the resistances have the same value:<br>![[Pasted image 20230611200349.png]]
- They have to be all the same value because we also have considered this bridge a **balanced bridge**, so: $$\frac{R_4}{R_io} = \frac{R_3}{R_2} = K$$

And obviously if you select this value for $K$ ($K = 1$), you have that maybe the condition for linearity, which is this one:<br>![[Pasted image 20230611200406.png]]
Maybe it's not fulfilled. 

- Remember the actual condition for linearity (where we consider a small non-linearity maximum error $NL_{MAX}$) is:$$ 1+K \gt \frac{x_{MAX}}{NL_{MAX}}$$In this particular case we considered an enormous error $NL_{MAX} = 1 = 100\%$ that means that if the real value $V_{TH}$ is $100$ than the output value of the sensor is $200$, way too much.<br>Usually we consider $NL_{MAX} = 0.1$

And so linearity requires large value of $K$ unless $x_{\text{MAX}}$ is very small, like in the strain gauge, instead ==$K=1$ **is the condition for the maximum sensitivity**==:<br>![[Pasted image 20230611200501.png]]
- So for **Strain Gauges**, where the $x_{\text{MAX}}$ value is really smallere than one, then you can select this value and obtain also a linear bridge and everything is okay.
- For **RTD**, where the $x_{\text{MAX}}$ value may be large, then you can't usually take this value for the design of the bridge, you have to take into account first of all the linearity because linear behavior you know is a very good quality for a circuit because it makes it simple and allows for having very good model of its behavior. 