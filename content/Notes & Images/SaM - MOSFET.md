- ***Sources***:
	- [Youtube (simplest)](https://www.youtube.com/watch?v=Bfvyj88Hs_o)
	- [Youtube (more detailed)](https://www.youtube.com/watch?v=rkbjHNEKcRw)
---
##### Graph
![[Pasted image 20240222161034.png|666]]

---
###### Memory Card
![[Samsung_SaM_Notes_00_240516_154329.jpg]]

---
##### Meaning of MOSFET

***MOSFET***: *Metal Oxide Semiconductor Field Effect Transistor*.

---
##### Types of MOSFETs
| MOSFET "type" or "mode" | n-type                               | p-type                               |
| ----------------------- | ------------------------------------ | ------------------------------------ |
| **Enhanced mode**       | ![[Pasted image 20240222153409.png]] | ![[Pasted image 20240222153429.png]] |
| **Depletion mode**      | ![[Pasted image 20240222153501.png]] | ![[Pasted image 20240222153517.png]] |
- "***n-type***": the body is of n-type lightly doped silicon, while ==**source** (**S**) and **drain** (**D**) are of  **n-type heavely doped silicon**==.
- "***p-type***": the body is of p-type lightly doped silicon, while ==**source** (**S**) and **drain** (**D**) are of  **p-type heavely doped silicon**==.
- "***Enhanced type***": ==the "***channel***" (or "channel region") forms when $V_{GS}$ is great enough==, and allows the passage of current from **source** (**S**) to **drain** (**D**).
- "***Depletion type***": the "***channel***" (or "channel region") is formed when the **MOSFET** is created, so it's a doped $n$-type region, ==when $V_{GS}$ is low enough, the channel is closed== and no current will flow from **source** (**S**) to **drain** (**D**).

---
##### Terminology (for N-MOSFET)
- **S**: Source (heavely doped $n^+$ region).
- **D**: Drain (heavely doped $n^+$ region).
- **G**: Gate (metal).
- **Body** or **Substrate** (lighlty doped $p$ region).
- **Oxide**: acts as an insulator between the **body** and the **gate** (**G**) terminal.
- ==The **MOSFET is symmetrical**==: **source** (**S**) and **drain** (**D**) can be interchanged, the defintion of **source** (**S**) is the terminal connected internally with the substrate:<br>![[Pasted image 20240222154513.png|333]]
- $V_{DS}$: voltage between **drain** (**D**) and **source** (**S**):![[How Does a MOSFET Work？V_{DS}.mp4]]- $V_{GS}$: voltage between **gate** (**G**) and **source** (**S**):![[How Does a MOSFET Work？V_{GS}.mp4]]
- ***Linear Region***:<br>![[Pasted image 20240222160439.png|333]]
- ***Saturation Region***:<br>![[Pasted image 20240222160541.png|333]]
- ***Drain Characteristics*** & ***Transfer Characteristics***:![[How Does a MOSFET Work？Characteristics of a Mosfet 1.mp4]]![[Pasted image 20240222161034.png|500]]

---
##### Enhanced type N-MOSFET 

***Construction***:<br>![[Pasted image 20240222155147.png|333]]<br>![[Pasted image 20240222104552.png|333]]<br>![[Pasted image 20240222104617.png|333]]<br>![[Pasted image 20240222104654.png|333]]

***Structure***:<br>![[Pasted image 20240222104737.png|333]]

***Workings***:<br>![[Pasted image 20240222104909.png|333]]<br>![[Pasted image 20240222105012.png|333]]<br>![[Pasted image 20240222105057.png|333]]<br>![[Pasted image 20240222105117.png|333]]<br>![[Pasted image 20240222105155.png|333]]<br>![[Pasted image 20240222105216.png|333]]<br>![[Pasted image 20240222105325.png|333]]<br>