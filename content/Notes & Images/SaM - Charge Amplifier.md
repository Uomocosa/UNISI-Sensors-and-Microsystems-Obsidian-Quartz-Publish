##### ***Remeber***:

> This is the [circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3YBMBWELrLJRAOMA2AdkmMUUnzQBYRVlJaBTAWjDACgBDEAZnx3D4GVHAwIMBYVK1RZ4cEIQw4hiMCMKIAnHirIWhKOHmR2Ac179whSnwGIqDJ+wDulyVRp2QWyqYBO7j6UIgy+RnJw7ADGQSIgoQkCTrDyWukZmVlaULCEyCqQWoQ8VPlgPJBghjAIrkHh3vGmbonhic31bSGigs6tveK0uH1Q9d7qXuTgnmMAHmg4kg68VBBIhjQrAJIAdgAOAK4ALuwL9JTqiLSE63oJ1CAA8odHp0A) for a "**charge amplifier**":<br>![[Pasted image 20240116225312.png|333]]
> - ==An [[SaM - Operational Amplifier|operational amplifier]] with capacitive feedback==.

> ![[Pasted image 20240514121542.png|333]]
> - If we ignore $R_f$:$$V_{out} = - {Q \over C_f}$$
> - If we consider $R_f$:$$V_{out} = - {Q \over C_f}\cdot e^{-{\large{t \over \tau}}}$$Where: $\tau = R_f \cdot C_f$.
> - ***Source***: [Wikipedia](https://it.wikipedia.org/wiki/Preamplificatore_di_carica)

> Take for example the output of a [[SaM - Ultrasonic Transducers (Piezoelectric Device)|piezoelectric ultrasonic transducer]], it's a charge:$$Q_p = K \kern0px d \kern2px x$$Described in "[[SaM - Complete Piezoelectric Device (Actuator + Sensor)|piezoelectric actuators]]" and "[[SaM - Capacitive Ultrasonic Transducers • CMUT Probes|ultrasonic tranducers]]".
> This charge is then converted to a voltage.
> To aid to this conversion, some special kind of amplifiers, called charge amplifiers where developed: =="_A **charge amplifier** is an **electronic current integrator**, that produces a voltage output proportional to the integrated value of the input current_"==.
> This is effectevely a measurement of the electrical input charge:$$V_{out} = - {q_{in} \over C_f}  = - {K d \kern2px  x \over C_f}$$*Source*: [Youtube](https://www.youtube.com/watch?v=xj4EKAAvXjM).

> **Advantages** of a charge amplifier:
> - The output voltage is proportional to the charge produced by the piezoelectric transducer.
> - The amount of charge present is not affected by the cable capacitance.
> - The sensititivity as well as the time constant are independent of the capacitance of the crystal, and aslo that of the connecting cables.
> 
> **Disadvantages** of a charge amplifier:
> - The **signal to noise ratio** (***SNR***) tends to be small.
> - The natural frequency of the transducer is reduced due to loss of stiffness caused by what amounts to a short circuit across the crystall.
>
> *Source*: [Youtube](https://www.youtube.com/watch?v=xj4EKAAvXjM).

> A charge amplifier is often used with a [[SaM - Piezoelectric Devices|piezoelectric sensor]].
> Here's a simple scheme: (*Source*: [Wikipedia](https://en.wikipedia.org/wiki/Charge_amplifier))
> ![[Pasted image 20240117122133.png|500]]
> - The sensor is a [[SaM - Piezoelectric Devices|piezoelectric one]]
> - $C_C$ is the "**cable** capacitance".
> - $C_{\text{inp}}$ is the "**inpedance** capacitance", we described it as $Z_{eq}$ for the [[SaM - AT-Cut Quartz|AT-cut quartz]].
> - $C_f$ and $R_f$ are the "**feedback** impedance".
> - $q_{in}$ and $q_{f}$ input charge and feedback charge, also:  $q_{f} = - q_{in}$.
> - The output formula is:$$V_{out} = -{q_{in} \over C_f}$$Where: $q_{in}$ depends on: the sensor, and the capacitances $C_C$ and $C_{inp}$.
> - The feedback resistor $R_f$ discharges the capacitor. <br>Without  $R_f$  the DC gain would be very high so that even the tiny DC input offset current of the operational amplifier would appear highly amplified at the output.
> - $R_f$ and  $C_f$ set the lower frequency limit of the charge amplifier:$$f_{\min} = {1 \over 2 \pi R_f C_f}$$

> Here's another version of the same circuit:
> (_Source_: [Youtube](https://www.youtube.com/watch?v=xj4EKAAvXjM))<br>![[Pasted image 20240117161441.png|500]]
> - This version is more similar to how we discribed the [[SaM - AT-Cut Quartz|AT-cut quartz]], and the [[SaM - Piezoelectric Accelerometer|electric circuit for a piezoelectric accelerometer]].

---
###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_3.jpg]]

---
