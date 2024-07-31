##### ***Remeber***:

> Let's take into consideration a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|one-quarter resistive bridge]], and add the wire resistance to the sensor, like so:<br>![[Pasted image 20230625114046 1.png|333]]
> The output formula will become:$$V_{TH} = V {R_0 (1 + G\varepsilon) + 2R_{{\small W}}\over 2 R_0 + R_0G\varepsilon + 2R_{{\small W}}} - {V\over 2}$$So we have an offset equal and sensitivity equal to: #NOT_SURE_ABOUT_THIS (redo the sensitivity calculations)$$ \begin{array}{l} \text{Offset}:&\left.V_{TH}\right|_{\varepsilon = 0} = V {\large{R_0 + 2R_{{\small W}}\over 2 R_0 + 2R_{{\small W}}}}  \\[3px] \text{Sensitivity}:&\left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = V {\large{R_0 \kern2px G\over 2 R_0 + 2R_{{\small W}}}}\end{array}$$The offset **in theory could be corrected**.
> However the sensitivity is different from the nominal one.
> And both offset and sensitivity depend on the wire resisitance, so both value can change,  a **variable offset** and a **variable gain**, are errors that I **cannot correct**.

> If we use a [[SaM - Voltage Supply vs. Current Supply|current supply]], and we cople the read-out, like so:<br>![[Pasted image 20230625114138.png]]
> We have that the sensitivity (also called "gain" if we consider ${1 \over V}{dV_{TH}\over d\varepsilon}$ instead of ${dV_{TH}\over d\varepsilon}$) now is fixed, however we still have a **variable offset**:$$ \begin{array}{l} V_{TH}= I_{DC} R_0 (1 + G\varepsilon) + I_{DC} \kern2px 2 R_{{\tiny W}} - I_{DC} R_{0} \\[7px] \text{Offset}: \kern40px \left.V_{TH}\right|_{\varepsilon = 0} = I_{DC} \kern2px {2R_{{\small W}}} - I_{DC} R_0  \\[3px] \text{Sensitivity}: \kern5px \left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = I_{DC} \kern1pxR_0 \kern1px G \end{array}$$Since we have an [[SaM - AC-Coupled Amplifier|AC-coupled read-out]], if for a single measurement the offset remains the same (so it is a **DC offset**), we will discard it.
> ==This is a good solution for **AC measurements**==.

> Instead if we have space to add another cable, we can use a **3 wires layout**, and still use a [[SaM - Voltage Supply vs. Current Supply|voltage supply]], like so:<br>![[Pasted image 20230625114149 1.png|333]]
> By adding another cable **we can compleately remove the offset**: #NOT_SURE_ABOUT_THIS (redo the sensitivity calculations)$$ \begin{array}{l} V_{TH} = V {\large {R_0 (1 + G\varepsilon) + R_{{\small W}} \over 2 R_0 + R_0 G\varepsilon + 2 R_{{\small W}}}} - {\large{V \over 2}} \\[5px] \text{Offset}: \kern40px \left.V_{TH}\right|_{\varepsilon = 0} = 0 \\[3px] \text{Sensitivity}: \kern5px \left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = V{\large{G R_0 (R_{{\small W}} + R_0) \over \left(2R_{{\small W}} + 2 R_0\right)^2}} \end{array}$$However, the sensitivity still depends on $R_{{\small W}}$.

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_2.jpg]]

---
##### 2 Wires Layout 

![[Pasted image 20230625114046.png]]

Calculating $V_{TH}$ it is equal to:<br>![[Pasted image 20230625114105.png]]

So we have an offset equal and gain to:
![[Pasted image 20230625114111.png]]
- ==And so what happens is that, I have an offset, which **in theory could be corrected**==.
- ==I have a sensitivity, which is **different from the nominal one**==.
- But the most, problematic aspect is that these values may vary, so I have both a **variable offset** and a **variable gain**, and this is an error that I **cannot correct**.

If I use a current supply instead of a voltage supply:<br>![[Pasted image 20230625114132.png]]
- I will have a **variable offset**.
- The offset will depend on the parasitic resistances, **but the gain is fixed**.
- ==So the gain will **NOT** depend on what happens in the cables==. 

So this is a good solution for **AC measurements**: when we use strain gauges for AC measurement (**for vibrations signal**), then this is a good solution, because by coupling the output of the bridge in an AC way to a differential amplifier:<br>![[Pasted image 20230625114138 1.png]]- ==The $I_{DC} \kern2px 2 \kern2px R_W$ part will be neglected==.

---
##### 3 Wires Layout 

![[Pasted image 20230625114149.png]]
![[Pasted image 20230625114159.png]]
- ==So in this case, **you don't have offset**==.
- ==So you cancel the offset, **but you still have a small variation of the of the gain** of the bridge==.

