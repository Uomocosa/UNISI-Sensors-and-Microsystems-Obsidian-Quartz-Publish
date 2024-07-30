##### ***Remeber***:

> The reason [[SaM - Ultrasonic Transducers (Piezoelectric Device)|ultrasonic transducer]] vibrates is beacuse a **standing wave** resonates inside of the piezoelectric cristal.
> _~ For example let's take a slice of **PZT**, in contact with *air* (which as a high [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|acustic impedance]])._
> We can imagine a **standing wave** like so:<br>![[Pasted image 20230720162328 1.png|500]]
> - A standing wave is a **resonance**.
> - We can represent it with a [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|formula]], and we have that the **forward part** of the wave ($U_{F}$) and **backward part** ($U_B$) assume:$$U = U_F+U_B = A \sin\left({2\pi x_1 \over \lambda_w}-\omega t\right) + A \sin\left({2\pi x_1 \over \lambda_w}+\omega t\right)$$Where:
> 	- $\lambda_w$ is the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wavelength]].
> 	- $t$ is the **time**, in the picture there is also another $t$ there it means thickness.
> 	- $x_1$ is the direction of propagation of the wave: we have limited it between $[-{t \over 2} \div {t \over 2}]$, here $t$ means **thickness**.

> _~Ex: Here a real world example of a **standing wave**_:<br>![[Pasted image 20230925195247.png|500]]
> You can see how it is described by the formula:$$U = A \sin\left({2\pi x_1 \over \lambda_w}-\omega t\right) + A \sin\left({2\pi x_1 \over \lambda_w}+\omega t\right)$$

---

And what happens actually is that we have in the PZT a **standing wave** is created, and the frequency of the standing wave is corresponding to the resonance that we have found in our simple analysis:
![[Pasted image 20230720162328.png]]
- The vibration of the surface is given by this standing wave.
- The standing wave comes from waves which propagate in the piezoelectric material, and it is the reusult of their superimposition.
- If you consider to have air as the surrounding material, the stress transmitted to the air is approximately $0$.
- I have also written the formula for a standing wave $U_W$ in case of a planar sine wave.
- What I see from outside is that this surface vibrating in time.
- So our coarse approximation can be used in order to understand what happens but taking to account that we have actually this small complex situation inside we don't have a slice which simply moves something which is related to a field inside it.
- ***What is a Standing Wave?***
	- A standing wave is a type of wave pattern that occurs when two waves of the same frequency and amplitude traveling in opposite directions superpose (combine) in such a way that they interfere with each other, creating a stationary or "standing" pattern.
- ***Example of Standing Wave***:
	- Here is a simple demonstration of a standing wave formed at different **specific** frequencies, here we have the 2nd 3rd and 4th armonics:![[Pasted image 20230925195139.png]]<br>![[Pasted image 20230925195214.png]]<br>![[Pasted image 20230925195247.png]]
	- **Source**: [Youtube](https://www.youtube.com/watch?v=-gr7KmTOrx0)