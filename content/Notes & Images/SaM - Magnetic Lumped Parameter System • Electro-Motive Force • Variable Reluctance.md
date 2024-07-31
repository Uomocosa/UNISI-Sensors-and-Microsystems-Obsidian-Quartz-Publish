##### ***Remeber***:

> - One of the most important advantages is that they **usually give a very large signal as an output**.
> - **They are also robust**.

> We define as we have done previously for the other [[SaM - Lumped Parameter Systems|lumped parameter systems]] an effort quantity (analog to the voltage in an electrical system), and a flow quantity (analog to a current), so for :
> - **Effort quantity**: $\text{MMF}$ (*Magneto Motive Force*) $\left[\text{A}\cdot\text{turn}\right]$ (**ampere** $\cdot$ **turns**, since it is found multipling the current per the number of turns of a inductance).
> - **Flow quantity**: $\phi(B)$ *(Flux of the Magnetic Field)* $\left[V \cdot s\right]$ (**volt** $\cdot$ **seconds**).

> This is the basic structure of a magnetic circuit:<br>![[Pasted image 20230719112102.png|500]]
> - $l_g$: length of the gap.
> - **PM**: *permament magnet*.
> - A magnetic circuit is made of a material which is **ferromagnetic**, we call this whole lump of ferroelectric material "the **core**".<br>For reference: *An electrical circuit is a conductive circuit*.
> - A **ferromagnetic material** is defined a such if it has a $\mu_r\gg 1$.<br>*~ For example pure iron at $99.8\%$ has a $\mu_r = 2\cdot 10^3$, while if it is pure at $99.95\%$ it has a $\mu_r = 2\cdot 10^5$*. #IMPORTANTE<br>This way we can consider **the filed** $B$ to be enclosed in the core, and $B=0$ outside.<br>**NOTE**: This is similar to electrical circuit were the resisitivity of air and wire differ of around **seven orders of magnitude**, however for magnetic circuits the difference is not so big.
> - $S_C$  *core surface* (the pedix $_C$ will always refer to the core).
> - $l$ : length of the whole **core**, or magnetic circuit.

> - Since there is a **gap** in the **core** of a magnetic circuit, we actually have a "**broken core**".
> - We can imagine a uniform field across the core and instead at the gap we have a distortion of the field, so the field tends to enlarge.<br>However if we consider $l_g \ll l$  (so small gaps) ⇒ then we can imagine that the field shape is the same, and it's like similar to a current flowing trough:<br>![[Pasted image 20230719112119.png|500]]

> Here is the lumped parameter circuit for a magnetic circuit **without a permanent magnet**:<br>![[Pasted image 20230719112153 1.png|500]]
> Here are the formulas:$$\begin{array}{l}  \mathcal{R}_g = \large{l_g \over \mu_0 S_g}  \\[3px]  \mathcal{R}_c = \large{l \over \mu_{\small{C}} S_C}  \\[3px]  \phi(B) = \normalsize{\mu_0 \kern2px H_g S_g} = \normalsize{\mu_{\small{C}} \kern2px H_C S_C}  \end{array}$$Where:
> - $\mu_{\small{C}} = \mu_0 \kern2px \mu_r$ ([[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|permeability]] of the core).
> - $H$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field intensity]], also remember that $\mu \cdot H = B$.

> Instead a **permanent magnet**, can be modelled as a  voltage generator in series to a resistance, with values:<br>![[Pasted image 20230719112222.png|500]]
> So:$$\begin{array}{l}  \mathcal{R}_M = \large{l_M \over \mu_M S_M}  \\[3px]  \text{MMF} = \mathcal{R}_M \cdot \phi(B_r)  \\[3px]  \phi(B_r) = S_M \cdot B_r = \mu_0 \cdot S_M \cdot M_r  \end{array}$$
> Where:
> - $\mu_M = \mu_0 \kern2px \mu_{\text{magnet}}$.
> - $M$ is the **magnetization**, we can calculate it as:$$M = H \cdot \mathcal{X}_M$$
> - $\mathcal{X}_M = 1 + \mu_r$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic susceptibility]].

> 
> Then if we consider the complete magnetic circuit, **including a PM** (permament magnet):<br>![[Pasted image 20230719112237 1.png|500]]
> - ==I call this $v$ the **"electro-motive force" across the coil**==. #IMPORTANTE <br>***This is actual voltage measured in Volts, but has sign inverted with rispect to the actual voltage drop***.
> - We can see this voltage as the output of our system. 

> If we perform the calculation of the **electro-motive force**: $$v = -N{d\phi(B) \over dt}$$
> We can split the results into this two contribution:
> - **Variable Current**: $$-\frac{N^2}{\mathcal{R}_{TOT}}\frac{dI}{dt}$$
> - **Variable Reluctance**: $$\left(\frac{N^2}{\mathcal{R}_{TOT}^2}I+\frac{N}{\mathcal{R}_{TOT}^2}\text{MMF}_{eq}\right)\frac{d\mathcal{R}_{TOT}}{dt}$$
> - If one or both are variable in time I'll have a change in the output voltage.
> - *How can the reluctance be variable?*<br>⇒ ==For instance, if the length of the gap is variable==, this can be an example of a displacement sensor). 

> Here are some example on how we can create **magnetic sensors** using the principle of **variable current** and **variable reluctance**:
>  - [[SaM - VRS (Variable Reluctance Sensors)]].
>  - [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction]] (variable current). #NOT_SURE_ABOUT_THIS 
>  - [[SaM - Variable Transformers]] (variable current). #NOT_SURE_ABOUT_THIS 

---
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_1.jpg]]

---
# Index
- [[#Introduction to the Magnetic Circuit]]
- [[#Magnetic Circuit]]

---
##### Introduction to the Magnetic Circuit
![[Pasted image 20230719112036.png]]
- One of the most important advantages is that they **usually give a very large signal as an output**.
- **They are also robust**.

So in order to have a summary of what happens in this field, it is useful to introduce the **magnetic circuit**:
![[Pasted image 20230719112046.png]]
- So magnetic circuits are the analogous of electrical circuits, we will find a quantity which is **magneto motive force** (**MMF**).<br>Which is the **quantity similar to voltage**.
- **Flux of the field $B$** ($\phi(B)$) instead, which will be the analogous of current.
- Whereas the electrical circuit model the reality very well, in this case instead for magnetic circuits, the **model is far less accurate**.
- The most **important laws** that we exploit to form this kind of circuit:
	- We take a curve $\Gamma$, which supports a surface $A$ with a normal (vector perpendicolar to the vector) in each point, which I call $\vec n$.<br>Then we consider current flowing through this surface $A$, the current is $I$ equal to:$$I = A \kern2px (\vec J  \cdot \vec n)$$Where: $\vec J$ is the current density vector.
	- If I take the line integral over $\Gamma$ of the magnetic field ($\vec H$), than we have that it is also eqal to $I$.<br>(Considering to have a static or no electrical field, so that ${\partial \phi(0) \over \partial t} = 0$)
- **NOTE**: In this example the surface $A$ is **generic**, it can be both defined as **closed** or **open**.

> **NOTE**:
> **Closed Surface**: means a surface that encloses a volume.
> **Open Surface**: means a surface that does not enclose a volume.

And then again, if I instead consider the integral of the electrical field on the line $\Gamma$:
![[Pasted image 20230719112054.png]]
- $E$ : is the voltage that I can measure along this line $\Gamma$.
- Remember that the flux $\phi(B)$ is the flux of the field $B$ over the surface $A$ ($A$: generic surface can be both closed or open).
- Finally remember that if I take a **closed** surface $A_{CLOSED}$, **so that encloses a volume**. we have that: the flux $\phi(B) = 0$.

---
##### Magnetic Circuit
Now let's take the structure of a magnetic circuit:
![[Pasted image 20230719112102.png]]
- $l_g$: length of the gap.
- A magnetic circuit is made of a material which is **ferromagnetic**.
- An electrical circuit is a conductive circuit, instead here we have a ferromagnetic circuit, so we consider a structure like this:
	- We take a **core** (the whole ferromagnetic material)
	- I place also a **permanent magnet** (**PM**)
	- And then I add a **gap**.
- So you have to imagine that this "C shape" is made of iron and closed with this permanent magnet here.
- I consider this to have a surface $S_C$  ($_C$ : Core), which is uniform all along the circuit, for simplicity.
- And I consider this gap to have a length $l_g$, which is much shorter than the overall length of the circuit ($l$). 

*Why this is a magnetic circuit?* 
⇒ Because I consider this to be a ferromagnetic material.
![[Pasted image 20230719112110.png]]
- Ferromagnetic material, are materials which have a **magnetic permeability** ($\mu_r$), which is much larger than $1$.
- *What does it matter?*<br>⇒ It means that we can consider, that if I put here a coil made up of $N$ turns, that wraps around the core, and I let a current $I$ flow through it, due to this permanent magnet, **the field $B$ is enclosed in the core**.<br>⇒ So it's like having a so different value of the B here outside the core and inside the core, that is like having $B = 0$ outside.
- **NOTE**: That this is similar to electrical circuit were the resisitivity of air and wire are around **seven orders of magnitude**, in case of magnetic circuits you don't have this exactly this situation, but with a certain approximation, we can think that the field $B$ is all here and follows the geometry of the core. 
- *What happens at the gap?*<br>⇒ We have a "**broken core**".<br>We can imagine a uniform field across the radio direction instead here we have a distortion of the field, so the field tends to enlarge.<br>For small gaps, we can imagine that the field shape is the same, and it's like similar to a current flowing trough, instead this time is the $B$ field which is enclosed here.

So now we can take a line which follows the shape of the circuit, and we can write the following:
![[Pasted image 20230719112119.png]]

The first assumption, **no permanent magnets**:
![[Pasted image 20230719112128.png]]
- $l_m$ (permaennt magnet length) equal to $0$.
- So in this case I can write selecting a curve $\Gamma$ which follows the shape of the core and I can evaluate the integral of the line integral $H$ over $\Gamma$.
- I suppose to have uniform value of the $H$ field over the line in the core and in the gap.<br>So different but uniform and all the field lines are parallel to gamma (so $\vec H \cdot \vec{dl} = H\kern2px dl$) 
- Now we can go on, and take a closed surface which has a cylinder shape like this ($\phi(B)$, shape defined by $S$ and $l$ both taken arbitrarly big to encapsulate the core), then I evaluate $\phi(B)$ the flux of the field $B$.
- We have:
	- $H_C$ (core) 
	- $H_g$ (gap) 
	- $\phi_{S_C}(B)$ (flux of the magnetic field $B$ over the core surface $S_C$) 
	- $\phi_{S_g}(B)$ (flux of the magnetic field $B$ over the gape surface $S_g$) 
- This means that ==the flux is the same in the gap and in the core==.

Now I can relate the flux $B$ with the value of the field inside, and we know that for instance the flux in the core of the field $B$ will be:
![[Pasted image 20230719112143.png]]
- I consider everything uniform, for simplicity.
- Since we have said $\phi_{S_C}(B) = \phi_{S_g}(B) = \phi(B)$ I will just call it $\phi$ for readability.
- **NI** is called the **magneto motive force** and is treated like a **voltage**, 
- $\phi$ the flux of $B$ is treated like a **current**.

So here is the magnetic circuit:
![[Pasted image 20230719112153.png]]
- $\varnothing S_c$ : diameter of the surface $S_c$
- I have two different components for my magnetic circuit since I have diregraded this permanent magnet, so I have to define two reluctances:
	- Reluctance of the core ($\mathcal{R_C}$)
	- And then the reluctance of the gap ($\mathcal{R_g}$)
- And instead of resistances, we have **reluctances gap** and **reluctances core**.

So now we are ready to place back our permanent magnet into our circuit:
![[Pasted image 20230719112222.png]]
![[Pasted image 20230719112213.png]]
- **PM** : Permanent Magnet
- $\phi(B_r)$ : flow generated by the magnet itself, which is due to the residual magnetic field (the magnetization of the magnet).
- $M_r$ : is the magnetization of the magnet.
- $_M$ (index) : thing realted to the magnet.
- I did this very large gap, but you have to think that this should be a small distance.
- The permanent magnet will have both a relucatnce (it is a piece of ferromagnetic material), but it will also have its own magneto motive force ("voltage") generator.

The permanent magnet can be inserted in the circuit, replacing its equivalent, which is for sure a reluctance:
![[Pasted image 20230719112242.png]]
- So we have a complete model of this circuit where I placed both a coil and a magnet as sources for the $B$ field.

So I write it again:
![[Pasted image 20230719112237.png]]
![[Pasted image 20230719112257.png]]
- I call this $v$ the electro-motive force across the coil (this is actual voltage measured in Volts, but has sign inverted with rispect to the actual voltage drop).
- Where:
	- MMF derived by $N I$
	- MMF$_{eq}$ derived by the permanent magnet.
- We can put something as an external circuit, something here it could be a generator and a resistance or other pieces of **electrical circuit**.
- So now we can also describe the effect of the magnetic behavior on the electrical circuit because ==we know that for **induction** these are coupled==.


More calculations:
![[Pasted image 20230719112306.png]]
![[Pasted image 20230719112314.png]]
- So at the end we can split the  **electro-motive force** total into this two contribution:
	- **Variable Current**: $$-\frac{N^2}{\mathcal{R}_{TOT}}\frac{dI}{dt}$$
	- **Variable Reluctance**: $$\left(\frac{N^2}{\mathcal{R}_{TOT}^2}I+\frac{N}{\mathcal{R}_{TOT}^2}\text{MMF}_{eq}\right)\frac{d\mathcal{R}_{TOT}}{dt}$$
- If one or both are variable in time I can read the output as a voltage.
- *How can the reluctance be variable?*<br>⇒ ==For instance, if the length of the gap is variable==, this can be an example of a displacement sensor).
