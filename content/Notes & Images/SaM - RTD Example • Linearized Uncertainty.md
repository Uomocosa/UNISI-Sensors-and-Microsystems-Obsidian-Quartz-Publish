##### ***Remeber***:

> - This is the circuit:<br>![[Pasted image 20231124180519.png]]
> - [Here's it the circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENxiVxCqU88PKsXBImSMPHggALNFJkUCQhji91s+aQJ5lMlKRXlJU9rOzc0ghPxBWQIsGKfIpVOQoxKVayBsnQ-MT62MSQGGCYUeAsAE4g2DZCCUneUOCSLADu5txgvLmc3JDZdgLJiXkFJTmVyTIWySUAbimWyoVpVO7d0BDdUNAIpQ2WKDKdHTVtdh1gXLOEUCyt8+1La+AYSwMyvf3pMMPxm2mbFgMmLADmRQlod9jYO8sAXhl5C8x5MhPcACZ0ABmbAArgAbAAuDFedAAdnRYjcPndvnZ8Ic4iiwL8UXhLvAWAAlPFUQgTfGHWS0KlHUqbHETNGM5YABwotnsNkETyW2Ex7IZuM2lP53RY7Lq+SodVFApmaTqvIS8tGi0KyrFywAHrIIjwRIRCBIvLJwIIAOJsACWcIAOgBnAD2QMdkIAFtaHY62ABbVng61A62Ix12gCOjtYutwf2YCVCdhxZrAgiJAAoACoAShYQA) with numerical values (not with real world values tho):<br>![[circuit-20231124-1811.png]]
> - So if we calculate the output of this circuit it will be:$$V_{RTD} = (V_{REF}-V_{io})\cdot\left(1+{R(t)\over R_{REF}}\right) - (V_{REF}-V_{io}+V_{id})$$Or it can be rewritten as:$$V_{RTD} = (V_{REF}-V_{io})\cdot{R(t)\over R_{REF}} - V_{id}$$

---

> - ==**NOTE**: The professor found another formula, where it also conisdered the gain of the A.O., so a formula also depending on $G_0$==.<br>This is a simpler formula, where I considered $G_0 = \infty$ and $A_0=1$, so that it can be remembered more easily.
> - The complete formula would be:$$V_{RTD} = A_0\left[\left(V_{REF}-V_{io} - {V_{out}\over G_0}\right){R(T) \over R_{REF}}- V_{id}\right]$$Where $V_{out}$ is the output of the A.O.

---

> -  Rememebr that we can see $R(T) = R_0(1+AT)$, using the [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen Equation]].
> - So the complete formula for this RTD circuit depends on:
> 	1. $V_{REF}$
> 	2. $V_{io}$
> 	3. $V_{id}$
> 	4. $V_{out}$
> 	5. $V_{RTD}$
> 	6. $R_0$
> 	7. $A$
> - So each of this parameter bring an **uncertanty**: $u(V_{REF}$), $u(V_{io})$, $\ldots$, $u(A)$, we can define the **combined unceranty**, or ***uncertanty on the measurament*** as: $$u(T) = \left|{\partial T \over \partial V_{REF}}\right|u(V_{REF}) + \left|{\partial T \over \partial V_{io}}\right|u(V_{io}) + \ldots + \left|{\partial T \over \partial A}\right|u(A)$$
> - Here are some real world values and names for some of this uncertanties:
> 	- $u(V_{REF})$ : "*drift of the reference voltage*".
> 	- $u(V_{io})$ : "*drift offset*" for the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100]] it is about $\simeq 10\mu\text{V}$. #IMPORTANTE 
> 	- $u(V_{id})$ : "*drift offset*".
> 	- $u(V_{RTD})$ or $V_{LSB}$ : "*Voltage at the Least Significant Bit*".
> - So if we perform some calculations we obtain that: $$u(T) \le {R_{REF}\over R_0 \kern2px A_0 \kern2px A \kern3px V_{REF}}\cdot 10 \ \mu\text{V}$$

---

- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENxiVxCqU88PKsXBImSMPHggALNFJkUCQhji91s+aQJ5lMlKRXlJU9rOzc0ghPxBWQIsGKfIpVOQoxKVayBsnQ-MT62MSQGGCYmDKu8CwATiDYNkJJKd5Q4CYsAO7m3GC8+ZzckLl2AqnJBUVledWpMhapZQBuaZbKxRlU7r3QEL1Q0AjlTZYoMeN2XXUdM4QlC1As7WBcy+sFGItDMv2DmTCjiVubGxZDJmUA5kuX99i7KwBeWQUbzAUyMdwAJnQAGZsACuABsAC4MF50AB2dHiLDuXyWKPsvQS73APyxeCucQASriqIQYnijrJaBTjuUzmAcSj6TEygAHCi2ew2QS4GLYI5I9ncyAxLlJJ78tl0hkbcl8jHImV8SYgcny+bERbYPAxDUS+aFKgNXVylZ3BoPLW8tB6hoZc3Wk2s7pdaYW-l3V3WmSkpLWjFAA) (With 2 A.O.):<br>In this Circuit the output is capped at $15$**V**, that is the source voltage of the amplifier ($V_{CC}$), so it does not depend on the sensor, you need a differential amplifier, with limited gain.<br>![[circuit-20231124-1725.png]]
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENxiVxCqU88PKsXBImSMPHggALNFJkUCQhji91s+aQJ5lMlKRXlJU9rOzc0ghPxBWQIsGKfIpVOQoxKVayBsnQ-MT62MSQGGCYUeAsAE4g2DZCCUneUOCSLADu5txgvLmc3JDZdgLJiXkFJTmVyTIWySUAbimWyoVpVO7d0BDdUNAIpQ2WKDKdHTVtdh1gXLOEUCyt8+1La+AYSwMyvf3pMMPxm2mbFgMmLADmRQlod9jYO8sAXhl5C8x5MhPcACZ0ABmbAArgAbAAuDFedAAdnRYjcPndvnZ8Ic4iiwL8UXhLvAWAAlPFUQgTfGHWS0KlHUqbHETNGM5YABwotnsNkETyW2Ex7IZuM2lP53RY7Lq+SodVFApmaTqvIS8tGi0KyrFywAHrIIjwRIRCBIvLJwIIAOJsACWcIAOgBnAD2QMdkIAFtaHY62ABbVng61A62Ix12gCOjtYutwf2YCVCdhxZrAgiJAAoACoAShYQA) (With an A.O. and an Ideal Differential Amplifier):<br>![[circuit-20231124-1811.png]]
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENxiVxCqU88PKsXBImSMPHggALNFLESeMBhQpiysDNnzSBPAkIz1iwZKksATiGwJuYXjbsgUhqOHMsA7rOz3HMn6c3JDeLgJCTv5UoT620b4JoQBuUS5ugdyuhO5UMjHQEDFQ0AhhmS4o2hXZUGHx6TlgXI11qc1Zbh3gGDnF+SVFuaVWwa3dfsXmoQDmY5Pz2H11AF4e9i3M9jLa3AAmdABmbACuADYALgwrdAB2dJYsc1tjL2iCMaMvWtoveFPwFgAJXWIH+ICMYOKeVouRKZR83R+oORoQADhCqi58CBVHwcdhciwMUidmNwYTPnMEGBuLhtDS6WgiT5eIJ3pjdjjYhCcbTBGzsR9RozwPxeWZxVRpiLaZUGXL6e4ZdZRWpqkF1crAaq5d0Kt1pYCfKLuqapewKHKOYKOWYxGAJFI4C5oDIFOoZBhiIZJNgHK73Rp3fhCFpiJAEORpnAWAAjWRkjBIIwQWzCgAesijEJEYfIqlk4EEABEAJaHQ4PO4XMtsM4AHQAzgBBAC2aLOFbLD2JaQcVAaihsRIx5sEMkh-JHnzH1qx+UHzkpdQxDVqDWwSxndSAA) (With an A.O. and a Non-Ideal Differential Amplifier):<br>![[circuit-20231124-1729.png]]<br>![[circuit-20231124-1730.png]]

---
##### Professor's Notes

![[Lecture 9_230926_222449_11 2.jpg]]
- The formula for $V_{RTD}$, i don't think it's correct. #NOT_SURE_ABOUT_THIS

---

![[Pasted image 20230717114450.png]]
![[Pasted image 20230717114513.png]]
![[Pasted image 20230717114459.png]]
![[Pasted image 20230717114529.png]]

---
##### All Quantities Contributing to the Uncertainty
![[Pasted image 20230717114544.png]]
![[Pasted image 20230717114555.png]]
![[Pasted image 20230717114606.png]]

---
