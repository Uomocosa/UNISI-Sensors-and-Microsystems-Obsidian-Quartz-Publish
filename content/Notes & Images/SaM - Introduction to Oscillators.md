##### ***Remeber***:

> - The basis of an oscillator is a circuit like this:<br>![[Pasted image 20230719114724 1.png|333]]
> - Not only that but we want it to have a **AC output** even if $V_s = 0\, \text{V}$.
> - To do this we first define the input-output transfer function:$${V_0 \over V_S} = {A \over 1 + \beta A}$$As we can see from this formula to have a "diverging output", so that the transient part does not decay, we need two things, we will later see more in detail in the [[SaM - Barkhausen Conditions|Barkhausen Conditions]]:$$\begin{array}{l} |\beta A | \ge 1 \\ \angle{\beta A} = 180° \end{array}$$

> - In an oscillator, I want a $V_{out}$ which is **unstable** or **marginally stable**.<br>So with a [[SaM - Modes Related to Conjugate Poles|couple of poles which are complex and conjugate]], and contrary to [[SaM - Stable Poles|stable poles]], we actually need:$$\operatorname{Re}{(p_1)} = \operatorname{Re}{(p_2)} \ge 0$$Actually, we can make a distinction between two outcomes:<br>![[Pasted image 20230719114744 1.png|500]]
> 	- We can have: $\operatorname{Re}{(p_1)} = \operatorname{Re}{(p_2)} \gt 0$ : **unstable poles** ⇒ The output will become a **square wave** do to the $V_{\text{SAT}}$ voltage source.
> 	- Or instead: $\operatorname{Re}{(p_1)} = \operatorname{Re}{(p_2)} = 0$ : **marginally stable poles** ⇒ The output will become a **sine wave**.

---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_1.jpg]]

---
We have said that the AC excitation was given by a voltage generator, sometimes I called it **oscillator**.
![[Pasted image 20230719114724.png]]
- The base of oscillating circuit is a **feedback circuit**.
- So we have to refer to the simple schematic of an amplifier $A$, and a feedback network $\beta$, which is sent to the input with a negative feedback
- Iwant also to put here this two terminals, ($\pm V_{cc}$), because this is a network where we have an **active device**, an amplifier, which is provided by a continuous **DC power**.
- Then we have a **passive network**, which is the feedback network, which brings back the output voltage to input, with this node here.
- Every time we have used an operational amplifier, we use this kind of structure here.
- Usually the feedback loop is used to control the output, make sure that it converges to a certain value, assurign that the response is stable and the transient vanishes.<br>For oscillators is the opposite.
- **NOTE**: $A$ in this case is the gain of the amplifier, for definition it is:$$A = {V_0\over V_i}$$

Now we want to have a circuit which we don't provide the input for, so $V_S = 0$
==**We want to have a circuit which provides a variable output with no input**==.
![[Pasted image 20230719114744.png]]
- What we want is therefore a circuit which is not stable since we want that with the signal input equal to zero, the output signal is a wave, an AC wave.
- Two types I can accept:
	- A **sine wave**.
	- Or a **square wave** (actually I'll only have this if I take into account the nonlinear behavior, so I'm out from the normal modeling).
- I want a $V_{out}$ like this, which is **unstable** or **marginally stable** with a **couple of poles which are complex and conjugate**.
- So I need a couple of complex conjugated poles with **real part, larger or equal to zero**.
- ==When I take into account this kind of situation, I will have that the response to the initial condition, or the transient response in any case will **never finish**, will be persistent and this is what I need from a **oscillator**==.

---