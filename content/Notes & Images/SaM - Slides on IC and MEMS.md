# Index
- [[#MEMS - Introduction]]
- [[#Silicon]]
- [[#IC Techonology]]
- [[#IC - Silicon Substrate (Wafer)]]
- [[#IC - Thin Film Deposition]]
- [[#IC - Doping]]
- [[#IC - Wet & Dry Etching]]
- [[#IC - Photolithography]]
- [[#IC - Evolution of the Density of Transistor]]
- [[#MS (Two Technologies)]]
- [[#MEMS - Surface Bulk Micromachining]]
- [[#MEMS - Anisotropic Etching]]
- [[#Comparison between Inosotropic and Anisotropic Etching]]
- [[#IC - Etch-Stop]]
- [[#Basic Structures for Bulk Micromachining]]
- [[#Preassure Sensor]]
- [[#Cantilever]]
- [[#Accelerometer]]
- [[#Surface Micromachining]]
- [[#Force Primary Sensor (Balance)]]
- [[#Capacitive Accelerometer]]
- [[#Complex Micromachine]]
- [[#MEMS - Accelerometer]]
- [[#MEMS - Accelerometer Chip View]]
- [[#MEMS - Gyroscope]]
- [[#MEMS - Pressure Sensor (Lecture Recap)]]
- [[#MEMS - Flow Sensor]]
- [[#Microphone]]
- [[#Where to Find Accelerometer (Real World Vendor Site)]]

---
##### MEMS - Introduction
![[Pasted image 20230719105846.png]]
![[Pasted image 20230719105851.png]]
![[Pasted image 20230719105855.png]]
- ==The difference between IC technology and MEMS technology, is that MEMS derives some steps, but then *add some steps which are not so standard as the IC technology*==.<br>This is the most important thing.
- ==*So, MEMS are developed using the normal route which is used for IC, but then there are some special steps which are used*==.

---
##### Silicon
![[Pasted image 20230719105859.png]]
![[Pasted image 20230719105906.png]]
![[Pasted image 20230719105910.png]]

---
##### IC Techonology
![[Pasted image 20230719105914.png]]
![[Pasted image 20230719105918.png]]
- ***What does LIGA means when we talk about special processes for MEMS creation?***
	- ==LIGA is an acronym that stands for *Lithographie, Galvanoformung, and Abformung*, which translates to **Lithography**, **Electroplating**, and **Molding** in English.<br>It refers to a specialized process used in the creation of microelectromechanical systems (MEMS)==.
	- ==The LIGA process is a combination of techniques that enables the fabrication of high-precision and high-aspect-ratio microstructures==.<br>It is particularly suited for the production of microstructures with complex geometries and tight tolerances.
	- Here's a brief overview of the three steps involved in the LIGA process:
	  1. Lithography: The first step in the LIGA process is lithography, which involves the use of photolithographic techniques to pattern a photoresist material.<br>A photosensitive resist is deposited onto a substrate, and a mask or pattern is used to selectively expose and develop the resist, forming a precise pattern of the desired microstructure.
	  2. Electroplating: After lithography, the patterned resist serves as a mold or template for the electroplating process.<br>The substrate with the patterned resist is immersed in an electroplating bath containing the desired metal or material.<br>An electric current is applied, causing the metal ions in the bath to deposit onto the exposed areas of the substrate, growing the microstructure layer by layer.<br>This electroplating step allows for the creation of high-aspect-ratio structures.
	  3. Molding: The final step of the LIGA process is molding, where the electroplated microstructure is separated from the substrate.<br>The resist material is typically dissolved or removed, leaving behind the free-standing microstructure.<br>The molded microstructure can then be further processed, assembled, or integrated into MEMS devices.
	- The LIGA process offers several advantages for MEMS fabrication, including the ability to produce complex 3D structures with high precision, repeatability, and scalability.<br>The process is often used in applications that require intricate microstructures, such as microfluidics, micro-optics, and microsensors.
	- It's worth noting that LIGA is just one of the many specialized processes used in MEMS fabrication.<br>Other techniques, such as surface micromachining, bulk micromachining, and silicon-on-insulator (SOI) technology, are also employed depending on the specific requirements of the MEMS device being manufactured.

---
##### IC - Silicon Substrate (Wafer)
![[Pasted image 20230719105927.png]]
![[Pasted image 20230719105933.png]]
- ==*Masks protect the wafer with the exception of the single region that has to be modified*==.
- ==*So when we design a chip, we actually desing different masks one for each step which can be doping, depositing or removing the film*==.

ICs are integrated circuit which are developed with the planar technology.
So it is all obtained on top of a substrate, a substrate which is a **pure silicon slice**, also called ***wafer***.
Some regions of the slice of the wafer are modified from a point of view of electrical properties by **doping**.
And we know that by creating a doped region we may have **resistors**, **diodes** and **transistors**.
And then there is a **deposition of the wires** and the connection between the different devices which are created with doping, and these are obtained by deposition of metal.

And since we need many, many metal wires, then we need also to **insulate some regions** in order to avoid electrical contact, and so also **oxide films are deposited**.
And obviously the process that it is used in order to create different regions with different properties needs also to **remove some layers of material**, and this is done by a process which is called **etching**.
So placing films and etching some part of the films.
So depositing and etching at the end we can get the overall structure of the circuit.

And here you can see for instance a cross section of a **[[SaM - MOSFET|MOSFET]]**:
So two doped regions are needed for **drain** and **source**, then ther is a **thin layer of oxide** below the **gate**.
And then there are these metal lines here which are **drain, gate and source contact**.
Instead the drain layer is an insulator.
So this placement of different regions is done through the design of **masks**.

---
##### IC - Thin Film Deposition
![[Pasted image 20230719105937.png]]
![[Pasted image 20230719105942.png]]
![[Pasted image 20230719105949.png]]
- ==*So by heating this target with ions, some of the metal atoms are extracted from the film, and then they are deposited on the silicone wafer, and with this you can create very, very thin metal layers*==.

---
##### IC - Doping
![[Pasted image 20230719105953.png]]
==*Here we see the ion implantation that is that the impurities, the dopants, are placed in the silicone lattice by means of "impinging" accelerated ions.
So for instance, phosphor or others are accelerated by an electrical field, and then they hit the silicone substrate, therefore they penetrate the lattice, and then after this process, the second process of annealing which is hitting, allows to the lattice to get back to a good order and you obtain in this way a doped material, as we can see in this figure here*==.
Mask protects the part you don't want to dope.
==So for this reason this is better than the fusion doping==.

---
##### IC - Wet & Dry Etching
![[Pasted image 20230719105957.png]]
- ==This is **wet etching** because it's done by chemical reaction in liquid phase==.

![[Pasted image 20230719110002.png]]
- ==Actually there is the possibility, also to remove something, by reactive ions which is a bombardment of oxidative ions, **dry etching**.<br>So the two possibilities, this is for sure more expensive, but more precise==.

---
##### IC - Photolithography
![[Pasted image 20230719110007.png]]
![[Pasted image 20230719110012.png]]
![[Pasted image 20230719110016.png]]
![[Pasted image 20230719110020.png]]
![[Pasted image 20230719110025.png]]

---
##### IC - Evolution of the Density of Transistor
![[Pasted image 20230719110029.png]]
![[Pasted image 20230719110033.png]]

---
##### MS (Two Technologies)
![[Pasted image 20230719110037.png]]
First of all:
- **MEMS** means **micro electro mechanical system**.
- **MS** is **micro sensor** so something which is more general, let's say.


---
##### MEMS - Surface Bulk Micromachining
![[Pasted image 20230719110042.png]]
![[Pasted image 20230719110046.png]]
- ==**Bulk micromachining**, the sensor's 3D structure is cut in the silicone substrate==.
- ==**Surface micromachining** allows to build a 3D structure **over** the substrate==.<br>So the wafer becomes a substrate, a backing, where on top of it the 3D structure is created.

---
##### MEMS - Anisotropic Etching
![[Pasted image 20230719105957.png]]
![[Pasted image 20230719110002.png]]
![[Pasted image 20230719110054.png]]
![[Pasted image 20230719110059.png]]
- We have two types of ***anisotropic etching*** which is **wet etching** and **dry etching**:
	- **Dry etching** is obtained with **bombardment of ions**, so plasma, which removes the silicone from some selected area, and the area are selected by masking as usual.
	- **Wet etching**, the same idea, remove the silicone using instead a **solution** with an etching compound.


---
##### Comparison between Inosotropic and Anisotropic Etching

But what we see here is the comparison between **anisotropic etching**, dry or wet, and **isotropic etching**, wet or dry.
- You see that in **anisotropic** etching, there is a control of the **side wall geometry**.
- Instead with **isotropic**, it's like having a sphere, so there is no control of the geometry of the side wall of the carving.

![[Pasted image 20230719110103.png]]
![[Pasted image 20230719110108.png]]
![[Pasted image 20230719110112.png]]
- ==Here you can see the clear difference between the two==.

![[Pasted image 20230719110117.png]]
- Wet etching which was the first process used to obtain micromachine sensor, is an etching process based on special chemical agents, which is *potassium hydroxide*.
- This is a special chemical reaction, which has an ==**etching rate** dependent on the direction with respect to the lattice of the crystal==.<br>That's why it is called **anisotropic**.

---
##### IC - Etch-Stop
![[Pasted image 20230719110122.png]]

---
##### Basic Structures for Bulk Micromachining
![[Pasted image 20230719110128.png]]
- ==So **bulk micro machining** is mainly used to obtain **membranes**==.

---
##### Preassure Sensor
![[Pasted image 20230719110132.png]]
![[Pasted image 20230719110139.png]]

---
##### Cantilever
![[Pasted image 20230719110149.png]]

---
##### Accelerometer
![[Pasted image 20230719110155.png]]

---
##### Surface Micromachining
Surface micro machining instead can be obtained with two types of processes:
![[Pasted image 20230719110200.png]]
- One is called "**one mask process**" and it's very simple, as you can see.

*But what happens if the process is not well controlled in terms of time?*<br>Maybe sometimes the encore is lost because there is the complete etching of the sacrificial layer or maybe it is too large and so the dynamics of the sensor is not so controlled.
⇒ So we arrived to the **two mask process** which has a better control of the "**anchor**".
![[Pasted image 20230719110205.png]]
- In this method, only the sacrificial layer is deposited then it is masked.

---
##### Force Primary Sensor (Balance)
![[Pasted image 20230719110212.png]]

---
##### Capacitive Accelerometer
![[Pasted image 20230719110215.png]]
![[Pasted image 20230719110221.png]]
![[Pasted image 20230719110228.png]]
![[Pasted image 20230719110237.png]]
![[Pasted image 20230719110241.png]]

---
##### Complex Micromachine
![[Pasted image 20230719110244.png]]
![[Pasted image 20230719110248.png]]
![[Pasted image 20230719110254.png]]

---
##### MEMS - Accelerometer
![[Pasted image 20230719110314.png]]
![[Pasted image 20230719110325.png]]
![[Pasted image 20230719110331.png]]
![[Pasted image 20230719110335.png]]
![[Pasted image 20230719110343.png]]
![[Pasted image 20230719110347.png]]
![[Pasted image 20230719110352.png]]
![[Pasted image 20230719110356.png]]
![[Pasted image 20230719110402.png]]
![[Pasted image 20230719110406.png]]
![[Pasted image 20230719110409.png]]

---
##### MEMS - Accelerometer Chip View
![[Pasted image 20230719110413.png]]

---
##### MEMS - Gyroscope
![[Pasted image 20230719110419.png]]
![[Pasted image 20230719110427.png]]
![[Pasted image 20230719110431.png]]


---
##### MEMS - Pressure Sensor (Lecture Recap)
![[Pasted image 20230719110438.png]]
![[Pasted image 20230719110443.png]]
![[Pasted image 20230719110446.png]]
![[Pasted image 20230719110450.png]]
![[Pasted image 20230719110454.png]]
![[Pasted image 20230719110458.png]]

This is what we have done during the lesson:
![[Pasted image 20230719110503.png]]
![[Pasted image 20230719110507.png]]
![[Pasted image 20230719110511.png]]
![[Pasted image 20230719110515.png]]
![[Pasted image 20230719110519.png]]
![[Pasted image 20230719110524.png]]
![[Pasted image 20230719110530.png]]

---
##### MEMS - Flow Sensor
![[Pasted image 20230719110534.png]]
![[Pasted image 20230719110541.png]]
![[Pasted image 20230719110545.png]]

---
##### Microphone
![[Pasted image 20230719110550.png]]

---
##### Where to Find Accelerometer (Real World Vendor Site)
![[Pasted image 20230719110556.png]]
- ==The most important one is that the front end is close to the sensor, so minimizes the influence of noise==. 
- ==The prices are very low==, because mass production is possible and therefore the prices can be really more compared to what we can find with traditional sensors.<br>That usually are more expensive because the production doesn't allow mass production. 
