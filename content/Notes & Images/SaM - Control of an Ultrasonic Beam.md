Especially in **biomedical fields**, a common technology to build [[SaM - Ultrasonic Beams|beam transducers]] is exploiting sources obtained by a raise of small transducer elements, because this allows both [[SaM - Ultrasonic Beam Stearing|beam steering]] and [[SaM - Focused Transducer for Ultrasonic Beams|focusing]].

==**Beam steering**: means reflection of the beam so change in the direction of propagation of the beam, of the ultrasonic field==.

So let's consider first of all how to focus, how to obtained focused beam by means of these kind of transducers.

You have a large surface, you have to imagine a rectangular source.
We call the lenght $l$, but acutally the tranducer is formed by **many different and independently excited elements**.
Each of these elements is an individual transducer with its own electrical excitation, so it is excited in an independent way.
![[Pasted image 20230720162719.png]]
- So you see that this is physically a planar structure.
- If we move this tranducer, further back as shown in the picture we can emulate the foused beam structure and obtain the same effect.
- However, since [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|the wave depends a linear relationship between time and space]], I don't need to physically move each transducer, because ==the only thing that is needed is to excite these single elements with a **time shift**==. #IMPORTANTE 
- $\Delta t_i$ is the delay that you will have to add, to simulate as if is the wave was generated by the transducer place on this curved surface.
- By deciding this different delays, it is possible to emulate different geometry of the source.

#IMPORTANTE 
This kind of solution requires a **complex transducer**, sometimes you have $128$ elements for instance which made up this probe, and complex because each of the transducer needs to be separated from the neighbor electrically.
Also you need wiring for each of them.
It becomes even more complex if we also want to make them also are recivers.

---
###### Memory Card
![[Samsung_SaM_Notes_19_240515_191312_2.jpg]]

---