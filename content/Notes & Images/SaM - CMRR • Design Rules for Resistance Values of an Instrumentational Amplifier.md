We start with the [[SaM - CMRR • Calculation of the CMRR for the Second Stage of an Instrumentational Amplifier|CMRR (Stage II)]], more specifically with $A_{1_{II}}$ and $A_{2_{II}}$ and we consider a non ideal [[SaM - Operational Amplifier|amplfiier]], specifically $A \neq \infty$, so we can write:$$\begin{array}{l}  A_{1_{II}} = {\huge{-\frac{R_2}{R_1}\frac{\beta A}{1 + \beta A}}} \\[3px]  A_{2_{II}} = {\huge{\frac{R_4}{R_3+R_4}\frac{A}{1 + \beta A}}}  \end{array}$$Where:$$\beta = {R_1 \over R_1 + R_2}$$We use the two following design rules: 
1. $A_1 = -A_2$ $\kern10px$ (So that we obtain an **infinite [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]]**)
2. $\large \frac{R_4}{R_3} = \frac{R_2}{R_1}  = \normalsize K$ $\kern10px$ (like for a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced bridge]])

So using the (1.) design rule, we can simplify $\frac{A}{1 + \beta A}$ from both terms, and we get:
$$\frac{R_2}{R_1} = \frac{R_4}{R_3+R_4}\frac{R_2 + R_1}{R_1}$$
Using the (2.) design rule:
$$K = \frac{K}{1+K}(K+1)$$And this is true $\forall \kern2px k \in \mathbb{R}$.
So if we ensure that $\large \frac{R_4}{R_3} = \frac{R_2}{R_1}$ we will have an infinite **CMRR**, even if the amplifier is not **ideal**.

---
###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_2.jpg]]

---