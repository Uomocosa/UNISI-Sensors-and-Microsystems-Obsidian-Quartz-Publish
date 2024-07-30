##### ***Remeber***:

> Piezoelectric coefficient matrix (in compact notation) for **PZT** (_Lead Zirconate Titanate_):$$\overline{\overline{d}}_{\text{PZT}} = \left[\begin{array}{l} 0 & 0 & 0 & 0 & d_{15} & 0 \\ 0 & 0 & 0 & d_{24} & 0 & 0 \\ d_{31} & d_{32} & d_{33} &  0 & 0 & 0 \end{array}\right]$$The real matrix dimensions are $[3 \times 3 \times 3]$.

>==_Piezoelectric materials have to be operated under the Curie temperature_==.

> **Curie Temperature**: _is the temperature at which, usually, there is a phase transition from an asymmetrical to a symmetrical crystal_.
> For ***PZT*** this temperature is $T_C = 250°\text{C}$.

---

Piezoelectric materials have to be **operated under the Curie temperature**, which is the temperature at which, usually, there is a phase transition from an asymmetrical to a symmetrical crystal, for PZT this temperature is 250 degrees, and etc.:
![[Pasted image 20230719124420.png]]
- **NOTE**: for quartz used at temperature higher than $200$ degrees its behavior becomes **highly dependent on temperature**.
- The last thing is that the structure of the $d$ matrix, which is the **charge piezoelectric coefficient**.<br>This matrix here actually has a **sparse** nature.
- For instance this is the shape that this matrix takes obviously with respect to the crystallographic axis, for PZT.
- Notice this is a matrix which is $3 \times 6$, while we defined it as a $3 \times 3 \times 3$, because it relates a vector to a tensor (which is a $3 \times 3$), so $3 \times 3 \times 3$, is the right dimension/size of the matrix, but since everything is symmetrical, the part related to the mechanical behavior, 2 indexes can be collapsed into one so in compact notation we can use for a couple of indexes the same rule that we have used for the elastic matrix.
- And you see here that we have many many zeroes, so ==only in some specific direction there is really a coupling between the electrical and mechanical response==.<br>(So a sparse matrix)
