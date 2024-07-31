##### ***Remeber***:

> Let's take for example the [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave definition]]:$$\rho \ddot{u}_{1} = c_{11} \frac{\partial^2 u_{1}}{\partial x_1^2}$$If we expand the $\ddot u_1$ term, we can write:$$\rho \frac{\partial^2 u_{1}}{\partial t^2} = c_{11} \frac{\partial^2 u_{1}}{\partial x_1^2}$$
> ==We have that the derivative over time and the derivative over space of a [[SaM - Ultrasonic Waves|wave]] have a **linear relationship**, they assume the same values only scaled of a factor $c_{11} \over \rho$==.<br>So if I define $U_1$ in such a way that this relationship is granted, I find that:$$U_1(t, x_1) = U_{1F}\left(t - \sqrt{\rho \over c_{11}}\cdot x_1\right) + U_{1B}\left(t + \sqrt{\rho \over c_{11}}\cdot x_1\right)$$We will se the meaning of each term.

> In the same media we can have two velocity for a [[SaM - Ultrasonic Waves|wave]] #IMPORTANTE :$$\begin{array}{l}  \text{longitudinal velocity:}& v_{\small l} = \sqrt{c_{11} \over \rho}  \\  \text{transverse velocity:}& v_{\small t} = \sqrt{c_{44} \over \rho}    \end{array}$$Where:
> - $c_{11}$ and $c_{44}$ come from the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor for isotropic materials]].
> - $\rho$ is the density of the material.
> - This two velocities relate to the [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave]] and [[SaM - Transverse Waves or Shear Waves|transverse wave]].
> 
> Usually we have that #IMPORTANTE :$$v_{\small l} \approx 2v_{\small t}$$

> So we can define the "components" of a [[SaM - Planar Waves or Plane Waves|generic planar wave]] ($U_1 ,\ U_2 ,\ U_3$, primitives of $\vec{\ddot{u}}$), as:$$\begin{array}{l} \text{longitudinal:} & U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right) + U_{1B}\left(t + \frac{x_1}{v_l}\right)   \\[5px]   \text{transverse:} & U_2(t,\, x_1) = U_{2F}\left(t - \frac{x_1}{v_t}\right) + U_{2B}\left(t + \frac{x_1}{v_t}\right)  \end{array}$$Where:
> - $U_1$ and $U_2$ are functions of any shape.
> - $U_{1F}$ and $U_{2F}$ : function of any shape that propagates **Forward**.
> - $U_{1B}$ and $U_{2B}$ : function of any shape that propagates **Backward**.
> - We consider only $U_1$ and $U_2$ since we need only to consider 2 components for a planar wave: the ones that move longitudinaly and the ones that propagates transverely to the propagtion of the wave ($U_3$ can just be incorporetad into $U_2$). #NOT_SURE_ABOUT_THIS

> For ultrasonic waves we can define the **wavelength** as: #IMPORTANTE $$\lambda_w = {v_l \over f_0}$$

> Here are some specific values for $v_l$ in different materials, and for $v_t$ in a **solid** (*Steel*): #IMPORTANTE ![[Pasted image 20230719131628 1.png|550]]
> - ==In solids the propagation of the wave is can be an order of magnitude higher that in fluids==.
> - For *Air*: $v_l \sim 340 \, {\text{m} \over \text{s}}$. #IMPORTANTE 
> - For *Steel*: $v_l \sim 6000 \, {\text{m} \over \text{s}}$ and $v_t \sim 3000 \, {\text{m} \over \text{s}}$. #IMPORTANTE 

> *Here's an example of a generic ultrasonic wave function: [[SaM ~ Example of an Ultrasonic Wave Function • Sine Plane Wave|the "sine plane wave"]]*. #IMPORTANTE 

> And from the *[[SaM ~ Example of an Ultrasonic Wave Function • Sine Plane Wave|"sine plane wave example"]]* let's focus on the formula:$$U_1(t,\, x_1) = A \sin\left(2\pi f_0\left(t-\frac{x_1}{v_l}\right)\right)$$Which is the period the wave fixed in time:![[Pasted image 20230719131639 1 1.png|500]]

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_2.jpg]]

---
Let's start with this formula:$$\rho \ddot{u}_{1} = c_{11} \frac{\partial^2 u_{1}}{\partial x_1^2}$$This is equal to:$$\rho \frac{\partial^2 u_{1}}{\partial t^2} = c_{11} \frac{\partial^2 u_{1}}{\partial x_1^2}$$==We have that the derivative over time and the derivative over space of a wave have a **linear relationship**, they assume the same values only scaled of a factor $c_{11} \over \rho$==.<br>So if I define $U_1$ in such a way that this relationship is granted, I find that:$$U_1(t, x_1) = U_{1F}\left(t - \sqrt{c_{11} \over \rho}\cdot x_1\right) + U_{1B}\left(t + \sqrt{c_{11} \over \rho}\cdot x_1\right)$$We will se the meaning of each term.


In the same media we can have two velocity for the wave:
![[Pasted image 20230925173121.png]]
- $v_l$ (longitudinal velocity) or $v_t$ (for trasverse or shear velocity).
- So in a fluid you can only have $v_l$
- Also $v_l \simeq v_t$
- Longitudinal or Planar wave case:
	- $U_1$ : function of any shape depending on $t$ (time) and $x_1$ (direction $1$).<br>**NOTE**: it is the primitive of the $u$ we have seen untill now, and it represents the "position" of the wave.<br>**NOTE**: a wave propagates as a difference of time and space, a wave has two velocity, one of propagation "how much fast it travels", and one of change "how fast it changes", the first is defined as we see before, the second by integrating over time (or space). #NOT_SURE_ABOUT_THIS 
	- $U_{1F}$ : function of any shape that propagates **Forward**
	- $U_{1B}$ : function of any shape that propagates **Backward**
- In the tranverse formula there is an error, I rewrite it: $$U_2(t, x_1) = U_{2F}\left(t - \frac{x_1}{v_t}\right) + U_{2B}\left(t + \frac{x_1}{v_t}\right)$$
- **NOTE**: the tranversal wave is $U_2$ and depends on $x_1$, **the indeces are important**.<br>Similar to the longitudinal wave were we have $U_1$ that depends on $x_1$.<br>We will analyze only one component of a wave: $U_i$ but remember that this waves can have $3$ components: $U_1$, $U_2$, $U_3$. #NOT_SURE_ABOUT_THIS 

For fluid we define better $v_l$:
![[Pasted image 20230719131628.png]]
- The **Bulk Modulus** is the same thing of $c_{11}$ and it is defined as ${P \over{\Delta V \over V}}$
- The we have some examples for different fluids.


> We have defined the **Bulk Modulus** in fluids which is the same thing as $c_{11}$ and it is defined as ${P \over{\Delta V \over V}}$. (*NOT IMPORTANT*) #NOT_SURE_ABOUT_THIS The [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|bulk modulus]] should actually be defined as: ${3 c_{12} + 2 c_{44} \over 3}$, while $c_{11} = c_{12} + 2 c_{44}$.


We take for instance a sine plane wave, and we take only a forward-propagating wave, so we define $U_{1F}$ that we said was a generic function as:
$$U_1(t, x_1) = U_{1F}(t - \frac{x_1}{v_l}) + 0 = A \sin(2\pi f(t-\frac{x_1}{v_l} + \varphi)$$
![[Pasted image 20230719131639.png]]
- We can define the wavelenght $\lambda$, related to both speed and frequency.
- $v_l$ : wave speed.
- At a fixed frequency $f$ ⇒ $\lambda$ depends linearly on the $v_l$, so the larger the speed the larger the wavelength.
- If we think about a small transduer **TX**, that vibrates at the frequency $f_0$ related to the ratio $\sqrt{\frac{K}{m}}$, so I generate the wave in the medium with a wavelenght $\lambda_{w}$ well known.
- The plot you see is a "photograph" of the wave, so the wave at a fixed time $t_0$, and you see how it propagates along $x_1$, and how the wavelength $\lambda_{w}$ is defined.
- We can use the wavelength or speed to find some difects in a material, since for example the wave travels in air 20 times slower than in steel, if a block of steel presents a pocket of air an ultrasonic sensor can find it.

---
##### Sine Plane Wave
![[Pasted image 20230720161946.png]]
- We consider it only going forward.
- We can also define the wave number: $K_{w}$, and the wave vector: $\vec K_{w}$

We can look at some values:
![[Pasted image 20230720162038.png]]
(this is considered the longitudinal transverse speed)

⇒ Therefore, ultrasonic transducers use different frequency to perform ultrasonic analysis in different media.

==For transverse wave, we have approximately half the wavelength, since $v_t \simeq {1 \over 2}v_l$==.

==The wavelength is an important parameter of the wave field==.
Sepending on the wavelength, different interaction with obstacle occurs.
So we can have a **reflection**, **scattering**, **diffraction**, ==depending on the ratio between the obstacle and the wave==.