##### ***Remeber***:

> Now we see a different circuit for an [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction|LVDT]], with a simple addition of a wire we obtain:<br>![[Pasted image 20230719114407.png|500]]
> - Just by adding a wire the [[SaM - Carrier Amplifier|carrier amplifier]] is no longer needed.
> - The two mutual inductances $M_1$ and $M_2$ of the two windings will be (using a linear approximation):
> 	- $M_1 = M_0(1+kx)$. #IMPORTANTE 
> 	- $M_2 = M_0(1-kx)$. #IMPORTANTE 
> 	- $kx$ this time is a little more complicated and it is defined as: $kx = {M_1 - M_2 \over 2 M_0}$<br>So: $M_1-M_2 = 2 M_0 k \kern2px x$
> 	- $M_0$ is the **mutual induction** of both $M_1$ and $M_2$ at rest.

> We will obtain as an ouptut two voltages, with different values, so a **differential output**.
> This two voltages can be converged into one using a [[SaM - Differential Amplifier|differential amplifier]].
> Here is a graph of the two output voltages for different values of $x$:<br>![[Pasted image 20230719114430.png|500]]

> With respect to the [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction|previous LVDT sensor]], this time we have a [[SaM - Differential Amplifier|differential amplifiers]], instead of a [[SaM - Carrier Amplifier|carrier amplifier]], but I need an additional [[SaM - Low Pass Filter|LPF]], and an **additional wire**, and this could be more complex in terms of connection and cabling.<br>⇒ ==Just becouse of cabiling issues, this solution here it's not always used==.

> Here's the ***IC for Read-Out of 5W LVDT***.
> **IC**: *Integrated Ciruit*
> **5W**: *5 Wires*
> **LVDT**: *Linear Variable Differential Transformer*<br>![[Pasted image 20230719114440.png|500]]
> - Specifically, we have used two [[SaM - Operational Amplifier|operational amplifiers]], and two [[SaM - Low Pass Filter|LPF]] (acting as rectifiers and for noise rejection #NOT_SURE_ABOUT_THIS ).
> - Finally we can compensate for both $T$ and $E_1$ thanks to the differential output, since:<br>$M_1-M_2 = 2 M_0 k \kern2px x$.<br>$M_1 + M_2 = 2M_0$.<br>And both outputs $A$ and $B$ depend on $E_1$.<br>==So the output will just depend on $kx$==.

---
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_4 1.jpg]]

---
![[Pasted image 20230719114407.png]]
- We just added a reference to ground between the two seondary windings.

Tho just by doing that the carrier amplifier is no longer needed:
![[Pasted image 20230719114421.png]]
![[Pasted image 20230719114430.png]]
- We will obtain as an ouptut two voltages, equal and opposed, so a **differential output**, they can be converged into one using a simple differential amplifier.
- So what happens is that I put two different amplifier, and then I need an additional wire, and this could be more complex in terms of connection and cabling.<br>⇒ Just becouse of cabiling issues, this solution here it's not always used.

---
##### IC for Read-Out of 5W LVDT
**IC**: *Integrated Ciruit*
**5W**: *5 Wires*
**LVDT**: *Linear Variable Differential Transformer*
![[Pasted image 20230719114440.png]]
- **NOTE**: Instead of a simple differential amplifier we have used two **Operational Amplifiers**, actually 2 Op.Amp plus 2 Rectifier.
- After those we have 2 [[SaM - Low Pass Filter|LPF]].
- This way we also "isolate" the output from the value of $E_1$.
