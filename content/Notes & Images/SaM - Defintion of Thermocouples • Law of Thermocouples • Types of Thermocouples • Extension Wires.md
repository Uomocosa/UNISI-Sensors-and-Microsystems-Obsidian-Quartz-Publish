##### ***Remeber***:

> ***Principle of a Thermocuple***:
> - Given a **conductive metal**, in a "***gradient of temperature***" (one end of the conductive metal is at different temperature then the other), the electrons with high temperature, so high energy, tends to diffuse towards the end with lowest temperature and vice versa.<br>**Therefore we have the establishment of an electrical field**.
> - So the gradient of temperature is converted into an electrical field, and the formula is:$$\vec E = \sigma(T) \cdot \nabla T$$Where:
> 	- $\nabla T$ defines the **[[Nabla Operand • Gradient • Divergence • Curl • Laplacian|gradient]] of temperature**.
> - Here's a basic example of the principle of a thermocouple:<br>![[Pasted image 20230719115316.png|500]]
> - $\sigma$ (the "***seebeck coefficient***"), **is not a constant, it is a function of temperature**.

> A **complete thermocouple** is given by at least two conductive wires of different materials, merged toghether to form a closed loop:<br>![[Pasted image 20230719115341 1.png|500]]
> - The reason we need two different conductive materials ($A$ and $B$), is because if we took just one type of materials, the voltage $\Delta V$ would be equal to $0$.
> - The really usefull thing about thermocouple, is that this voltage drop $\Delta V$ can be measure via a simple voltemeter, in any point of the termocouple. #NOT_SURE_ABOUT_THIS 

> We have then seen the **0-5 laws of thermocouple**: #IMPORTANTE 
> 
> 0. **Law of Homogeneus Metals**:<br>![[Pasted image 20230923000457.png|500]]
> 1. I only care about the two temperature **at the junctions** (between the two materials):<br>![[Pasted image 20230719115357.png|500]]
> 2. Any piece of material that at his junctions has the same temperature does not change the voltage drop:<br>![[Pasted image 20230719115415.png|500]]
> 3. Same as (*2.*):<br>![[Pasted image 20230719115428.png|500]]
> 4. **Law of Intermediate Metals**:<br>![[Pasted image 20230923000415.png|500]]
> 5. **Law of Intermediate Temperatures**:<br>![[Pasted image 20230923000440.png|500]]

> Here are some different types, they change in sensitivity, and temperature range, in total there are $8$ types: **K**, **J**, **T**, **N**, (**B**, **R**, **S**), **I**: #IMPORTANTE <br>![[Pasted image 20230719115516.png]]<br>![[Pasted image 20230719115535.png]]
> - With **T** being the most accurate ($68\frac{\mu V}{°\text{C}}$), and (**B**, **R**, **S**) having the largest range (up to $1800°\text{C}$). #IMPORTANTE 
> - If you take a standard **class 1** - **J type** thermocouples, then you have an accuracy of about $\pm 1.5°\text{C}$ at $350°\text{C}$. #IMPORTANTE 

> We can use thermocouples to measure temperatures at a somewhat large distance and having the voltemeter in a control room, here's an example:<br>![[Pasted image 20230719115554.png|500]]
> Now, if we need a particular material, for example to withstand high temperature, but said material cost a lot, we could cut costs using **extension wires**:<br>![[Pasted image 20230719115603 1.png|500]]
> - Suppose the material **A** and **B**, are extreamily costly, since in this example they have a high temperature range, we can save a lot of money if we change the material type in $D_1$ and $D_2$, placing them after **A** and **B** at $T_3$ where the temperature has cooled.<br>We will still measure the difference of temperatures between $T_1$ and $T_2$ (so no change whatsover), but we have cut costs by a lot.

---
###### Memory Card
![[Samsung_SaM_Notes_17_240515_185257_1.jpg]]
![[Samsung_SaM_Notes_17_240515_185257_2.jpg]]

---
# Index
- [[#Thermocouple]]
- [[#The 5 Laws of Thermocouples]]
- [[#Types of Thermocouples]]
- [[#Circuit Based on Thermocouples (Extensions Wires)]]

---
##### Thermocouple
![[Pasted image 20230719115316.png]]
- The electrons with high temperature, so high energy, tends to diffuse towards the end with lowest temperature and vice versa.<br>**Therefore we have the establishment of an electrical field**.
- So the gradient of temperature is converted into an electrical field.
- the "*seebeck coefficient*", **is not a constant, it is a function of temperature**.

![[Pasted image 20230719115327.png]]
- If sigma is constant, then I find the beautiful relationship which is this one.<br>Here it is a linear formula but it is not actually.
- This is the principle, the effect that we have described here is called "***thermoelectric effect***" or "***Seebeck effect***".

Now I can go and understand how to perform a measurement, exploiting this effect here:
![[Pasted image 20230719115341.png]]
- I can easily measure a voltage (with a voltimeter or somenthing)
- So, we have a temperature gradient along the wire, we define it taking the temperature in two points, so $T_1$, and $T_2$.
- In the first case I will have the same temperature because I'm looking at a closed situation, so no matter the gradient (if it is linear) the voltage drop will be $0$.
- Instead in the second situation, if I integrate along all the wire, so:$$\Delta V = \int_{T_1}^{T_1}\sigma dT \neq 0$$Can be measured since I used two different materials, with different **seebeck coefficient**.<br>In any case, what matters is the difference of temperature between the two junction points.<br>Actually this coefficient here contains also the contribution of the **Peltier** effect, which is a voltage localized at the junction, something which you have if there is a current flowing.<br>==So you'll have the ***Peltier effect*** only if you have a current otherwise, you can forget it==.

---
##### The 5 Laws of Thermocouples
![[Pasted image 20230719115357.png]]
- I only care about the two temperature **at the junctions** (between the two materials)

![[Pasted image 20230719115415.png]]
![[Pasted image 20230719115421.png]]
- You can introduce any other material in your circuit if you have the same temperature at the two new junctions, then this part here of the circuit doesn't matter, as long as the temperature is the same at the junction of $C$.

![[Pasted image 20230719115428.png]]
- Same as rule **($2$)**

![[Pasted image 20230923000415.png]]
- In the math form the integrals $\int_{T_1}^{T_2} \sigma_C dt$ and $\int_{T_2}^{T_1} \sigma_C dt$ are the same and of opposite sign, so it's fine.

![[Pasted image 20230923000440.png]]
- Similar to rule **($1$)**.

![[Pasted image 20230923000457.png]]
- We need to have at least a junction.
- **NOTE**: we imagine to have the reading of the voltage in just one point of the wire, if we put two voltimeters, one at $T_1$ and one at $T_2$ we will have a reading, but that is not the point of thermocouples, we want to use just one "voltimeter" at $T_1$ for example.

We also have this beautiful law here (some of the previous rules all in one):
![[Pasted image 20230719115504.png]]
-  I write the voltage $V_{AB}$ like this in order to understand that this is a couple of materials $A$ and $B$.
- That means that even if the measurement of a thermocouple is actually something which depends on two temperatures, **actually what matters is only their difference**.
- Then you can see that this kind of relationship here is actually **not linear**, we have already seen it and we can describe it in this way.
- he accuracy is usually about $1°C$, and moreover they measure the difference between two temperature, they are not absolute temperature devices.

---
##### Types of Thermocouples
Here are some different types, they change in sensitivity, and temperature range, in total there are $8$ types: **K**, **J**, **T**, **N**, **B,R,S** and **I**.
With **T** the most accurate ($68\frac{\mu V}{°C}$), and **B,R,S** with the largest range ($+1800°C$).
If you take a standard class 1 **J** type standard thermocouples, then you have an accuracy of about $\pm 1.5°C$ at $350°C$.
![[Pasted image 20230719115516.png]]
![[Pasted image 20230719115535.png]]


---
##### Circuit Based on Thermocouples (Extensions Wires)
![[Pasted image 20230719115554.png]]
![[Pasted image 20230719115603.png]]
![[Pasted image 20230719115620.png]]
- Suppose the material **A** and **B**, are extreamily costly, since in this example they have a high temperature range, we can save a lot of money if we change the material type in $D_1$ and $D_2$, placing them after **A** and **B** at $T_3$ where the temperature has cooled.<br>We will still measure the difference of temperatures between $T_1$ and $T_2$, so no change whatsover, but we have saved money.
- So extension wires are especially meant for **expensive thermocouples** where I can't do this right arrangement here I need to change material I can't select a material with a random choice, I have to using this special material which are called extension wires and are standard devices.

---
