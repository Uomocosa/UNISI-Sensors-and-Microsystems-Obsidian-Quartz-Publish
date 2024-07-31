#NOT_SURE_ABOUT_THIS 
In the context of capacitive sensors, the terms "grounded" and "ungrounded" refer to the way the sensing electrode is connected to the system.<br>Let's discuss the differences between grounded and ungrounded capacitive sensors in terms of their front-end requirements:
1. **Grounded Capacitive Sensors:**
   - **Connection:** The sensing electrode of a grounded capacitive sensor is connected to the ground reference of the system.
   - **Front-End Requirement:** The front-end circuit for a grounded capacitive sensor typically involves a simpler design.<br>It may use a single-ended amplifier since the reference is the ground.
2. **Ungrounded Capacitive Sensors:**
   - **Connection:** The sensing electrode of an ungrounded capacitive sensor is not directly connected to the ground reference.
   - **Front-End Requirement:** The front-end circuit for an ungrounded capacitive sensor is usually more complex.<br>It often involves a differential amplifier to measure the potential difference between the sensor electrode and the ground.

In summary, the choice between grounded and ungrounded capacitive sensors depends on the application requirements.<br>Grounded sensors are simpler to implement in terms of front-end circuitry, but ungrounded sensors may offer advantages in certain situations, such as when there is a need to isolate the sensor from the ground for safety or when dealing with specific noise conditions.

---
#NOT_SURE_ABOUT_THIS 
- Remember that for capacitive sensors, we have to distinguish always between:
  1. **Grounded sensor**, (remember about proximity sensors).<br>So this kind of sensor which has the requirement of having one of the two terminals referenced.
  2. And the other type are a **referenced sensors**.<br>In this case we are completely free to choose the best readout topology, because we have no constraints about the grounding of one of the two terminals.

---
