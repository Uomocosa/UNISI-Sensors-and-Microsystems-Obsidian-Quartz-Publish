##### ***Remeber***:

> A load cell is a sensor for force, it takes a force and changes into a strain, its strucutre is like this:<br>![[Pasted image 20240112173342.png|333]]
> It uses a [[SaM - Full Bridge|full bridge]] of [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gagues]], we can model it as:<br>![[Pasted image 20240112173532.png]]

> We have that:$$\begin{array}{l} \varepsilon_l={\large{\sigma_1 \over E}} \\[3px] \varepsilon_t= - \nu \varepsilon_l \\[3px] \sigma_1 = {\large{F_1 \over A}} \end{array}$$Where:
> - $E$ and $\nu$ are [[SaM - Young and Poisson Modulus|Young and Poisson modulus]].
> - $\varepsilon_l$ and $\varepsilon_t$ are the [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|longitudinal and tranverse strain]].
> - $\sigma_1$ is the [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]] in the direction of the force $F_1$.
> 
> While the [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauge]] can be modelled as:$$R = R_0 \kern2px (1 + G\varepsilon )$$We put four **strain gauges** in a **load cell**, and by changing their orientation (with respect to the direction of $F_1$) we can describe each of them as:$$\begin{array}{l} R_1 = R_0 \kern2px (1 + G\varepsilon_l ) \\ R_2 = R_0 \kern2px (1 + G\varepsilon_t ) \\ R_3 = R_0 \kern2px (1 - G\varepsilon_l ) \\ R_4 = R_0 \kern2px (1 - G\varepsilon_t ) \\ \end{array}$$Finally remember that a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|resistive bridge]] has this equation:$$V_{out} = V \left({R_1\over R_1 + R_4}-{R_2\over R_2 + R_3}\right)$$

> If we perform the calculations we obtain the formual of a load brige, refering to the strain:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px \varepsilon_l $$We can change the equation using force instead of strain:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px {E \over A} \kern2px F_1 $$Finally rember that usually $\nu \simeq 0.35$.

> ==As far as the effect of temperature is concerned, this is a full bridge because the elements are identical, and if they experience the same temperature, they vary in the same way, so **the effect of temperature is completely cancelled**==.
> "*A full bridge rejects common mode disturbances*"

---

![[Pasted image 20230625114207.png]]
- ==Primary Sensor for Force: Takes a force and changes into a strain==. 

Now we create a full-bridge with four sensors:<br>![[Pasted image 20230625114212.png]]
![[Pasted image 20230625114219.png]]
![[Pasted image 20230625114226.png]]
- Usually $\nu \simeq 0.35$ 

==As far as the effect of temperature is concerned, this is a full bridge because the elements are identical, and if they experience the same temperature, they vary in the same way, so **the effect of temperature is completely cancelled**==.

