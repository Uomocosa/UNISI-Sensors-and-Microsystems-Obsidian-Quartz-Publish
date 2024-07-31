##### ***Remeber***:

> When we described the [[SaM - Accelerometer|accelerometer]] we didn't account for the effect of gravity.
> If we wish to account for it:
> - If the sensor **does not rotate**: ==the effect is simply **having an offset**== (It will measure the external force $F_{\text{ext}}$ plus the gravity $g$).
> - Instead, if the sensor **rotates** during measurements then this $\theta$ here varies and therefore you have a variable error let's say with respect to what you want to measure which is the effect of gravity of the seismic mass itself, and you see that the larger is this mass $m_s$ and the worst is this effect.

> Also if the accelerometer is ==not mounted in a "*solid*" way==, so if my mount introduces some dumping or acts as a spring, it can be a problem:<br>![[Pasted image 20230710172353 2.png|500]]
>  - ==The transfer function of your device will not be the one that we have studied, but it will be this with some spurious resonance==:<br>![[Pasted image 20230710172353 1.png|500]]
>  - ==This has to be avoided==. 

---
###### Memory Card
![[Samsung_SaM_Notes_06_240515_120818_5.jpg]]

---
##### Effect of Gravity on the Accelerometer
![[Pasted image 20230710172154.png]]
![[Pasted image 20230710172222.png]]
![[Pasted image 20230710172238.png]]

- ==So the effect is simply: **having an offset**==.  
- Instead, if the sensor **rotates** during measurements then this $\theta$ here varies and therefore you have a variable error let's say with respect to what you want to measure which is the effect of gravity of the seismic mass itself, and you see that the larger is this mass $m_s$ and the worst is this effect.

---
##### Mounting an Accelerometer
If the accelerometer is not mounted in a "solid" way, so if my mount introduces some dumping or acts as a spring, it can be a problem:
![[Pasted image 20230710172353.png]]
- ==The transfer function of your device will not be the one that we have studied, but it will be this with some spurious resonance==. 
- ==This has to be avoided==. 