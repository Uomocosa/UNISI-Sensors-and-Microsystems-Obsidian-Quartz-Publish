> ***Remeber***:
> - This is the structure of the **Sigma-Delta Converter**:<br>![[Pasted image 20230719105708 1.png|500]]
> - ==For this converter you need a **not-referenced capacitive sensor**==.
> - [[#Understand How Sigma-Delta Converter Works]], here is a simpler formula, to remeber, to understand how it works:$$V_{out} = V_{ref} \cdot \frac{\text{\# of 1s}}{\text{\# of 1s} + \text{\# of 0s}}$$

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_7 1.jpg]]

---
![[Pasted image 20230719105651.png]]
![[Pasted image 20230719105708.png]]
- ==You have a **no referenced sensors**==

---
##### Understand How Sigma-Delta Converter Works:
***From Online Resource***: [Youtube](https://www.youtube.com/watch?v=M5Vx-X66seg)

![[Pasted image 20230920174300.png]]
![[Pasted image 20230920174232.png]]
![[Pasted image 20230920174424.png]]
![[Pasted image 20230920174622.png]]
- $u$ : paid amount each day (etiher $5€$ or $0€$)
- $y$ : is the average paid over $n$ days.
- $x$ : is the fixed price of the coffee.

![[Pasted image 20230920174930.png]]
- So $x$ is the input
- $u$ the fixed amount passed to the comparitor (either $V_{REF}$ or $0 V$)
- $y$ the "running average", it's possible to average 
- You can get the exact value of $x$ of the coffee only by averaging many samples.
- Here, what happens is that the $1$ bit, A/D, at the end, outputs a $0, 1, 0, 1, 1, \ldots$, sequence whose average value:$$V_{out} = V_{ref} \cdot \frac{\text{\# of 1s}}{\text{\# of 1s} + \text{\# of 0s}}$$ is actually the analog voltage input $V_x$, so $V_out \simeq V_x$. 
- The precision of the average is decided by how many bits I use to sample a single signal $V_x$.

---