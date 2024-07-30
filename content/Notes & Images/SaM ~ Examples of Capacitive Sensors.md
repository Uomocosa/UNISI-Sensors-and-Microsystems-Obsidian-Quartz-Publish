# Index
- [[#Electric Microphone]]
- [[#Proximity Sensor and Touch Screen]]

---
##### Electric Microphone
A special example of a **capacitive microphone** is the **electric microphone**.
![[Pasted image 20230719105816.png]]
- In this case the dielectric is a **ferroelectric material**.<br>This ferroelectric material has the property of being **permanently polarized**, it's like a permanent magnet but it's permanent in the electrical domain, we don't need a source voltage.<br>Tho we do need an amplifier afeterwards, to be able to read the output.
- So this is a very simple structure of a microphone, where we don't need an excitation.
- $C_{COUP}$ is a coupling capacitance, it is needed because everything here is [[SaM - AC-Coupled Amplifier|AC-coupled]], because we know that our signal is only a varying signal, ==we don't need to carry the DC values==, we can filter them out.

---
##### Proximity Sensor and Touch Screen
![[Pasted image 20230719105821.png]]
![[Pasted image 20230719105825.png]]
- How a touch screen can be arranged with contact which are rows and columns and the measuring of the capacitance between an individual row and a colon reveals the presence of the finger.

Also something about the readout circuit which can be used in conjunction with the sensor depending on the specific problem:
- **oscillator** or **locking circuit** (a circuit that helps maintain a stable and reliable output signal from the capacitive sensor).
- **AC base circuit** that we have divided into **FM** and **AM** circuits.
- **Switching Capacitance**.
- **$\Sigma-\Delta$ A/D Converter**.

==The most important problem to be taking into account, is the effect of the **electric noise** and so it is required the presence of **shielding**, If the sensor is far from the frontend<br>Tthis problem is far less dramatic if instead you have the sensor close to the front end electronics==.
